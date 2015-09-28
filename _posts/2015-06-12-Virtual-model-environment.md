---
layout: post
title: Virtual model environment
navid: Blog
category: kidney
tags: ['modelling', 'whole-kidney']
---

Thanks to Daniel Hurley from the University of Melbourne
[Systems Biology Laboratory](http://uomsystemsbiology.github.io/), the
[whole-kidney model]({{ site.baseurl }}{% post_url 2014-01-15-Hormonal-regulation-of-salt-and-water-excretion %})
that I produced with S.&nbsp;Randall Thomas is now available as a
[virtual environment](https://github.com/uomsystemsbiology/rgm_kidney_vagrant)
that is straightforward to install and get running.

1. Ensure that [Git](https://git-scm.com/),
   [Vagrant](http://www.vagrantup.com) and
   [VirtualBox](https://www.virtualbox.org/) are installed; then
2. Run the following commands in a terminal:

{% highlight bash %}
git clone https://github.com/uomsystemsbiology/rgm_kidney_vagrant.git
cd rgm_kidney_vagrant
vagrant up
{% endhighlight %}

This will open a virtual machine that includes the pre-compiled model
executable, allowing you to run model simulations and reproduce any of our
manuscript figures by double-clicking on a desktop icon!
