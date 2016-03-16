---
layout: page
navid: Tools
title: Plotting with D3
---

This is a (hopefully simple) tutorial that will show you how to build a basic
interactive plot using the [D3.js](http://d3js.org/) javascript library.
Familiarity with basic HTML, CSS and JavaScript is assumed; there are many
online classes you can take (e.g., [Codeacademy](http://www.codecademy.com/))
if you aren't familiar with any of these.

The various files that are produced in this tutorial are available for
download; see the bottom of this page for the links.

## The data

Shown below is an example of a simple data file that defines two series of
measurements ("A" and "B", as distinguished by the *exp* column) taken over
the course of several months (*date*).
For each measurement we have a *value* and an *error*.

{% highlight text %}
date,exp,value,error
2014-06-01,A,5.0,0.2
2014-06-01,B,6.0,0.3
2014-06-15,A,5.2,0.2
2014-06-15,B,6.0,0.2
2014-07-01,A,5.5,0.1
2014-07-01,B,6.2,0.5
2014-07-15,A,5.5,0.1
2014-07-15,B,6.5,0.3
2014-08-01,A,5.4,0.1
2014-08-01,B,7.2,0.8
2014-08-15,A,5.4,0.1
2014-08-15,B,7.0,0.4
{% endhighlight %}

## The basic page structure

Shown below is a simple web page that loads the D3.js library (lines 6--7),
provides a location for the plot (line 21) and loads the script that will
draw the plot (line 28).
The plotting script is loaded at the end of the file in order to ensure that
the browser will have finished loading the page content and the D3.js library
before calling the script.

{% highlight html linenos=table %}
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="Content-Type" content="text/html;charset=utf-8"/>
    <title>Example Plot</title>
    <script type="text/javascript" src="http://d3js.org/d3.v3.min.js"
            charset="utf-8"></script>
    <style media="screen" type="text/css">
        /* Display page content in a centred column. */
        #content { max-width: 60em; margin: 0 auto; }
        /* Centre headings and figure captions. */
        #content, h1, .caption { text-align: center; }
    </style>
  </head>
<body>
  <!-- Page content. -->
  <div id="content">
    <h1>Example Plot</h1>

    <!-- The plot will be created inside the following span element. -->
    <span id="plot1" class="chart"></span>
    <p class="caption">
      <strong>Figure 1:</strong> Some time-series data.
    </p>
  </div>

  <!-- Generate the plots. -->
  <script type="text/javascript" src="./plot.js" charset="utf-8"></script>
</body>
</html>
{% endhighlight %}

## Drawing a simple plot

The following script will produce a line plot of the two data series.
It can look overwhelming at first glance; there is a large amount of code
because D3.js is a general-purpose visualisation library, and is not
specifically designed for producing plots.
But don't worry, each block is relatively simple and performs a single task.

{% highlight js linenos=table %}
// Create a new namespace to contain all of the variables and functions.
var Plot = Plot || {};

// A standard linear numerical axis, with adjustable precision.
Plot.num_axis = function(label, precision, get) {
    return {
        get: get,
        scale: d3.scale.linear(),
        tick: 5,
        grid: 10,
        fmt_tick: function(d) { return d.toFixed(precision); },
        label: label
    };
}

// A date axis.
Plot.date_axis = function(label, get) {
    return {
        get: get,
        scale: d3.time.scale(),
        tick: d3.time.month,
        grid: d3.time.week,
        fmt_tick: d3.time.format("%Y-%m-%d"),
        label: label
    };
}

// A time axis, where the underlying data is in seconds and is displayed as
// MM:SS. Note that hours are not accounted for, the minutes simply increase.
Plot.time_axis = function(label, get) {
    return {
        get: get,
        scale: d3.scale.linear(),
        tick: 5,
        grid: 10,
        fmt_tick: function(secs) {
            var mins = Math.floor(secs / 60);
            secs = Math.round(secs - 60 * mins);
            if (secs < 10) {
                return mins + ":0" + secs;
            } else {
                return mins + ":" + secs;
            }
        },
        label: label
    };
}

// Draw a single plot.
Plot.draw = function(prep_data, plot) {
    // Determine the net dimensions of the plot.
    plot.net_w = parseFloat(plot.dims.w) + parseFloat(plot.dims.margin_x),
    plot.net_h = parseFloat(plot.dims.h) + parseFloat(plot.dims.margin_y)

    // Create the SVG element that will contain the plot.
    plot.svg_elt = d3.select(plot.selector)
        .append("svg:svg")
        .attr("width", plot.net_w)
        .attr("height", plot.net_h)
        .attr("preserveAspectRatio", "none");

    // Create the group element that will contain every plot component.
    plot.contents = plot.svg_elt.append("svg:g")
        .attr("transform",
              "translate(" + plot.dims.margin_x + ", 0)");

    // Perform any plot-specific data manipulation.
    if (plot.hasOwnProperty('get_plot_data')) {
        plot.data = plot.get_plot_data(prep_data);
    } else {
        plot.data = prep_data;
    }

    // Calculate the plot axis domains.
    plot.axis = {
        x_dom: d3.extent(plot.data, plot.x.get),
        y_dom: d3.extent(plot.data, plot.y.get)
    };

    // Enlarge the y-axis domain to account for error bars, if any.
    if (plot.hasOwnProperty('ymin') && plot.hasOwnProperty('ymax')) {
        plot.axis.y_dom[0] = Math.min(plot.axis.y_dom[0],
                                      d3.min(plot.data, plot.ymin));
        plot.axis.y_dom[1] = Math.max(plot.axis.y_dom[1],
                                      d3.max(plot.data, plot.ymax));
    }

    // Pad the axis domains so that points don't sit on the edges of the plot.
    // The Number() function is used so that the padding works for numeric
    // and date scales.
    var x_range = Number(plot.axis.x_dom[1]) - Number(plot.axis.x_dom[0]),
        y_range = plot.axis.y_dom[1] - plot.axis.y_dom[0];
    plot.axis.x_dom[0] = Number(plot.axis.x_dom[0]) - 0.025 * x_range;
    plot.axis.x_dom[1] = Number(plot.axis.x_dom[1]) + 0.025 * x_range;
    plot.axis.y_dom[0] = plot.axis.y_dom[0] - 0.025 * y_range;
    plot.axis.y_dom[1] = plot.axis.y_dom[1] + 0.025 * y_range;

    // Create the axis scales.
    plot.axis.x = plot.x.scale.domain(plot.axis.x_dom)
        .range([0, plot.dims.w - plot.dims.padding]);
    // Note: we reverse the range here, because in the default SVG coordinate
    // system the y-axis points *down* and reversing this gives us a y-axis
    // that points *up*, as we would normally expect.
    plot.axis.y = plot.y.scale.domain(plot.axis.y_dom)
        .range([plot.dims.h, 0]);

    // Draw the x-axis.
    plot.contents.append("svg:line")
        .attr("x1", plot.axis.x(plot.axis.x_dom[0]))
        .attr("y1", plot.axis.y(plot.axis.y_dom[0]))
        .attr("x2", plot.axis.x(plot.axis.x_dom[1]))
        .attr("y2", plot.axis.y(plot.axis.y_dom[0]));

    // Draw the y-axis.
    plot.contents.append("svg:line")
        .attr("x1", plot.axis.x(plot.axis.x_dom[0]))
        .attr("y1", plot.axis.y(plot.axis.y_dom[0]))
        .attr("x2", plot.axis.x(plot.axis.x_dom[0]))
        .attr("y2", plot.axis.y(plot.axis.y_dom[1]));

    // Draw the x-axis label.
    plot.contents.append("text")
        .attr("class", "xTitle")
        .attr("x", plot.dims.w / 2)
        .attr("y", plot.dims.margin_y + plot.axis.y(plot.axis.y_dom[0]))
        .attr("dy", "-0.4em")
        .style("text-anchor", "middle")
        .text(plot.x.label);

    // Draw the y-axis label.
    plot.contents.append("text")
        .attr("class", "yTitle")
        .attr("y", - 0.6 * plot.dims.margin_x)
        .attr("x", - plot.dims.h / 2)
        .attr("dy", "-0.8em")
        .style("text-anchor", "middle")
        .attr("transform", "rotate(-90)")
        .text(plot.y.label);

    // Draw the x-axis tick labels.
    plot.contents.selectAll(".xLabel")
        .data(plot.axis.x.ticks(plot.x.tick))
        .enter().append("svg:text")
        .attr("class", "xLabel")
        .text(plot.x.fmt_tick)
        .attr("x", function(d) { return plot.axis.x(d) })
        .attr("y", 0.5 * plot.dims.margin_y + plot.axis.y(plot.axis.y_dom[0]))
        .attr("text-anchor", "middle");

    // Draw the y-axis tick labels.
    plot.contents.selectAll(".yLabel")
        .data(plot.axis.y.ticks(plot.y.tick))
        .enter().append("svg:text")
        .attr("class", "yLabel")
        .text(plot.y.fmt_tick)
        .attr("x", - 0.25 * plot.dims.margin_x)
        .attr("y", function(d) { return plot.axis.y(d) })
        .attr("text-anchor", "end")
        .attr("dy", 4);

    // Draw the x-axis tick lines.
    plot.contents.selectAll(".xTicks")
        .data(plot.axis.x.ticks(plot.x.tick))
        .enter().append("svg:line")
        .attr("class", "xTicks")
        .attr("x1", function(d) { return plot.axis.x(d); })
        .attr("y1", plot.axis.y(plot.axis.y_dom[0]))
        .attr("x2", function(d) { return plot.axis.x(d); })
        /* Scale the size of the ticks relative to the y domain. */
        .attr("y2", plot.axis.y(plot.axis.y_dom[0]) + 0.2 * plot.dims.margin_y);

    // Draw the y-axis tick lines.
    plot.contents.selectAll(".yTicks")
        .data(plot.axis.y.ticks(plot.y.tick))
        .enter().append("svg:line")
        .attr("class", "yTicks")
        .attr("y1", function(d) { return plot.axis.y(d); })
        .attr("x1", - 0.125 * plot.dims.margin_x)
        .attr("y2", function(d) { return plot.axis.y(d); })
        .attr("x2", 0);

    // Plot the vertical grid lines.
    plot.contents.selectAll(".xGrid")
        .data(plot.axis.x.ticks(plot.x.grid))
        .enter().append("svg:line")
        .attr("class", "grid")
        .attr("x1", function(d) { return plot.axis.x(d); })
        .attr("y1",  plot.axis.y(plot.axis.y_dom[0]))
        .attr("x2", function(d) { return plot.axis.x(d); })
        /* Scale the size of the ticks relative to the y domain. */
        .attr("y2", plot.axis.y(plot.axis.y_dom[1]));

    // Plot the horizontal grid lines.
    plot.contents.selectAll(".yGrid")
        .data(plot.axis.y.ticks(plot.y.grid))
        .enter().append("svg:line")
        .attr("class", "grid")
        .attr("y1", function(d) { return plot.axis.y(d); })
        .attr("x1", plot.axis.x(plot.axis.x_dom[0]))
        .attr("y2", function(d) { return plot.axis.y(d); })
        /* Scale the size of the ticks relative to the y domain. */
        .attr("x2", plot.axis.x(plot.axis.x_dom[1]));

    // How to draw a line for a data series.
    plot.draw_line = d3.svg.line()
        .x(function(d) { return plot.axis.x(plot.x.get(d)); })
        .y(function(d) { return plot.axis.y(plot.y.get(d)); });

    // Draw a line for each data series.
    if (plot.hasOwnProperty('group')) {
        // Multiple data series, divide them into groups.
        var data_series = d3.nest()
            .key(plot.group)
            .entries(plot_data);
        // Plot each group separately.
        for (var i = 0; i < data_series.length; i++) {
            plot.contents.append("svg:path")
                .data([data_series[i].values])
                .attr("class", data_series[i].key + " series")
                .attr("d", plot.draw_line)
        }
    } else {
        // A single data series.
        plot.contents.append("svg:path")
            .data([plot.data])
            .attr("class", "series")
            .attr("d", plot.draw_line);
    }

    // Draw the error bars, if any.
    if (plot.hasOwnProperty('ymin') && plot.hasOwnProperty('ymax')) {
        plot.data.forEach(function(d) {
            var x = plot.axis.x(plot.x.get(d));
            var y1 = plot.axis.y(plot.ymin(d));
            var y2 = plot.axis.y(plot.ymax(d));
            var classes = "errorbar";
            if (plot.hasOwnProperty('group')) {
                // Identify the group to which this error bar belongs.
                classes = classes + " " + plot.group(d);
            }

            // Draw the vertical span of the error.
            plot.contents.append("svg:line")
                .attr("class", classes)
                .attr("x1", x)
                .attr("x2", x)
                .attr("y1", y1)
                .attr("y2", y2);
            // Draw the bottom (horizontal) line.
            plot.contents.append("svg:line")
                .attr("class", classes)
                .attr("x1", x - 5)
                .attr("x2", x + 5)
                .attr("y1", y1)
                .attr("y2", y1);
            // Draw the top (horizontal) line.
            plot.contents.append("svg:line")
                .attr("class", classes)
                .attr("x1", x - 5)
                .attr("x2", x + 5)
                .attr("y1", y2)
                .attr("y2", y2);
        })
    };

    // Draw points along the line.
    plot.data.forEach(function(d) {
        var classes = "point";
        if (plot.hasOwnProperty('group')) {
            // Identify the group to which this point belongs.
            classes = classes + " " + plot.group(d);
        }
        plot.contents.append("svg:circle")
            .attr("class", classes)
            .attr("cx", plot.axis.x(plot.x.get(d)))
            .attr("cy", plot.axis.y(plot.y.get(d)))
            .attr("r", 5)
    });
}

Plot.draw_many = function(data_file, prepare_data, plots) {
    // Asynchronously load the data file and prepare it for the plots,
    // then draw each plot in turn.
    d3.csv(
        data_file,
        function(error, data_rows) {
            if (error == null) {
                plot_data = prepare_data(data_rows);
                for (var i = 0; i < plots.length; i++) {
                    Plot.draw(plot_data, plots[i]);
                }
            } else {
                console.log(error);
            }
        });
}

// Calculate the plot width based on the width of the '#content' div.
var width = document.getElementById('content').offsetWidth * 0.6;
// Display plots with a 4:3 aspect ratio.
var height = 0.75 * width;

// Define the properties of the plot we want to produce.
var plot1 = {
    // The plot dimensions and margins.
    dims: {
        w: width - 75,
        h: height - 50,
        margin_x: 75,
        margin_y: 50,
        padding: 10
    },
    // The id of the HTML element that will contain the plot.
    selector: "#plot1",
    // Perform any plot-specific data manipulation.
    get_plot_data: function(data_rows) {
        // The plot data, as generated by prepare_data(), is ready to plot.
        return data_rows;
    },
    // Define the scales, labels and data associated with each axis.
    x: Plot.date_axis("Date", function(d) { return d.date; }),
    y: Plot.num_axis("Value (units)", 1, function(d) { return d.value; }),
    // Define the bounds of the error bars.
    ymin: function(d) { return d.ymin; },
    ymax: function(d) { return d.ymax; },
    // Define the key that identifies different data series.
    group: function(d) { return d.exp; }
}

// Prepare the raw data for plotting.
var prepare_data = function(data_rows) {
    var date_format = d3.time.format("%Y-%m-%d");
    data_rows.forEach(function(d) {
        // Convert dates from strings to date objects.
        d.date = date_format.parse(d.date);
        // Ensure that value is stored as a floating-point number.
        d.value = parseFloat(d.value);
        // Calculate the error bars for each data point.
        d.ymin = d.value - parseFloat(d.error);
        d.ymax = d.value + parseFloat(d.error);
    });
    return data_rows;
}

// Draw the plot(s).
Plot.draw_many("data.csv", prepare_data, [plot1]);
{% endhighlight %}

## Controlling the appearance of the plot

We now need to add some rules that define how the lines and paths will appear.

{% highlight css linenos=table %}
/* Draw all lines in black, by default. */
line { stroke: black; }
/* Draw very thin grid lines. */
.grid { stroke-width: 0.1; }
/* Draw thicker lines for the axes. */
.axis { stroke-width: 0.8; }
/* Draw slightly thinner lines for the axis ticks. */
.xTicks, .yTicks { stroke-width: 0.6; }
/* Draw data series with very thick lines. */
.series { stroke-width: 3; stroke: #afafaf; fill: none; }
/* Draw error bars with quite thick lines. */
.errorbar { stroke-width: 2; }
/* Draw black data points. */
.point { fill: black; stroke-width: 2; }
/* Colour data series, points and error bars on a per-group basis. */
.series.A, .errorbar.A, .point.A { stroke: #268bd2; }
.series.B, .errorbar.B, .point.B { stroke: #859900; }
{% endhighlight %}

## Highlighting a data series

With a few minor adjustments, we can now highlight a data series if the user
moves the mouse over that data series.
First, we define how a highlighted data series should appear, assuming that it
will be identified by having the identifier `highlight`.

{% highlight css linenos=table %}
/* Draw highlighted series with a thick red line. */
#highlight { stroke: #FF0000; stroke-width: 4; }
#highlight.point { fill: #FF0000; stroke: black; stroke-width: 2; }
{% endhighlight %}

We then need to define how to add and remove this highlighting.

{% highlight js linenos=table %}
    // Define how to highlight a particular data series.
    plot.highlight_group = function(group_class) {
        return function(d) {
            if (d3.select(this).attr("id") === "highlight") {
                /* Do nothing if the current series is already highlighted. */
                return;
            } else {
                /* Remove any previous highlighting from this plot. */
                plot.contents.selectAll("#highlight")
                    .attr("id", null);
                /* Highlight the selected series. */
                plot.contents.selectAll("." + group_class)
                    .attr("id", "highlight");
            }
        };
    };
{% endhighlight %}

And we need to trigger this highlighting when the mouse moves over a data
series.
Note that we only add this event handler in the case where there are multiple
date series.

{% highlight js linenos=table %}
        // Plot each group separately.
        for (var i = 0; i < data_series.length; i++) {
            plot.contents.append("svg:path")
                .data([data_series[i].values])
                .attr("class", data_series[i].key + " series")
                .attr("d", plot.draw_line)
                .on("mouseover", plot.highlight_group(data_series[i].key));
        }
{% endhighlight %}

## Adding a second plot

Let's now plot the mean values of the two data sets.
First, we need to create an element to contain this second plot.

{% highlight html linenos=table %}
    <!-- The plot will be created inside the following span element. -->
    <span id="plot2" class="chart"></span>
    <p class="caption">
      <strong>Figure 2:</strong> Mean time-series data.
    </p>
{% endhighlight %}

Then we need to define the properties of this second plot.
Note that we don't define *ymin* and *ymax*, because we're not going to plot
any error bars.

{% highlight js linenos=table %}
// Define the properties of the plot we want to produce.
var plot2 = {
    // The plot dimensions and margins.
    dims: {
        w: width - 75,
        h: height - 50,
        margin_x: 75,
        margin_y: 50,
        padding: 10
    },
    // The id of the HTML element that will contain the plot.
    selector: "#plot2",
    // Calculate the mean value at each date.
    get_plot_data: function(data_rows) {
        // Group the data points by date.
        var by_date = d3.nest()
            .key(function(d) { return d.date; })
            .entries(data_rows);
        // For each date, calculate the mean value.
        for (var i = 0; i < by_date.length; i++) {
            by_date[i].mean_val = d3.mean(by_date[i].values,
                                       function(d) { return d.value; });
            by_date[i].date = by_date[i].values[0].date;
        }
        return by_date;
    },
    // Define the scales, labels and data associated with each axis.
    x: Plot.date_axis("Date", function(d) { return d.date; }),
    y: Plot.num_axis("Mean value (units)", 1,
                     function(d) { return d.mean_val; }),
}
{% endhighlight %}

And finally, we add this to the list of plots to draw.

{% highlight js linenos=table %}
// Draw the plot(s).
Plot.draw_many("data.csv", prepare_data, [plot1, plot2]);
{% endhighlight %}

## Download the materials

The files that have been produced in this tutorial are available here:

- [The webpage](./files/index.html)
- [The data file](./files/data.csv)
- [The plotting script](./files/plot.js)

If you're interested in making more elaborate plots, there is a huge gallery
of [examples](https://github.com/mbostock/d3/wiki/Gallery) that you can use as
a starting point.
You can also look at the [source
code](https://github.com/robmoss/robmoss.github.io/tree/master/model/rfc) for
my interactive [acute renal function curves]({{ site.baseurl }}/model/rfc/).
