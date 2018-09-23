---
title: Model Documentation and Tools
---

As mathematical models grow larger and more complex they become harder to
analyse and understand.
Once a model is sufficiently complex, the likelihood of someone being able to
replicate its behaviour based on the model description in a publication
becomes negligible.
Making the model source code available is necessary but insufficient to render
a model comprehensible, hence the proliferation of
[semantic](http://sed-ml.org/) [markup](http://sbml.org/)
[languages](http://www.cellml.org/) and
[detailed](http://co.mbine.org/standards/miriam)
[guidelines](http://biomodels.net/miase/) to describe models and *in silico*
experiments.

The importance of clear, concise and
[helpful documentation](https://www.divio.com/blog/documentation/) is also
[paramount](http://jacobian.org/writing/great-documentation/) to ensuring a
published model and the accompanying simulations are sufficiently
well-described that the published results can be replicated independently of
the original model implementation.
It can be hard to write [good
prose](http://www.americanscientist.org/issues/id.877,y.0,no.,content.true,page.1,css.print/issue.aspx)
and to *teach* the user rather than simply
[telling them](http://stevelosh.com/blog/2013/09/teach-dont-tell/) what to do.
That's why it's important a have good editor; only edit the documentation
[yourself](http://lifehacker.com/5968996/how-to-edit-your-own-writing/all) as
a last resort.
Good documentation means that your model/software is
[learnable](http://brikis98.blogspot.com.tr/2014/05/you-are-what-you-document.html).

The discipline of software engineering has led to the production of a plethora
of languages, tools and processes that can help improve the design,
description and maintenance of a complex piece of software.
Below is a (very incomplete) list of languages and tools that I have found
helpful for the design, implementation, validation and documentation of
non-trivial mathematical models.

## Tutorials

- How to produce [interactive plots](./plotting-with-d3) using D3; last
  updated *2014-06-08*.

## Tools

### Mathematics

- [The R Project](http://www.r-project.org/) (and
  [contributed docs](http://cran.r-project.org/other-docs.html)) &mdash; a
  statistical computing and plotting tool
- [SymPy](http://sympy.org/) &mdash; a symbolic solver / computer algebra
  system (CAS)
- [SciPy](http://www.scipy.org/) &mdash; a suite of numerical science and
  engineering tools
- [GNU Octave](http://www.gnu.org/software/octave/) &mdash; a numerical solver
  and plotting tool, mostly Matlab-compatible

### Plotting

- [ggplot2](http://had.co.nz/ggplot2/) &mdash; an elegant and powerful
  plotting system for R
- [Gnuplot](http://www.gnuplot.info/) &mdash; a command-line plotting tool,
  also used by GNU Octave
- [PLplot](http://plplot.sourceforge.net/) &mdash; a plotting package with a
  number of language bindings
- [g3data](https://github.com/pn2200/g3data) (or
  [g3data2](https://github.com/jonasfrantz/g3data2)) &mdash; great for
  extracting data from published plots
- [D3.js](http://d3js.org/) (and
  [book](http://chimera.labs.oreilly.com/books/1230000000345/)) &mdash; a
  JavaScript library for creating interactive data-driven visualisations.

### Programming

-  [OCaml](http://caml.inria.fr/ocaml/)
   ([manual](http://caml.inria.fr/pub/docs/manual-ocaml/),
   [libraries](http://caml.inria.fr/pub/docs/manual-ocaml/libref/),
   [testing](http://ounit.forge.ocamlcore.org/),
   [examples](http://pleac.sourceforge.net/pleac_ocaml/))
- [JoCaml](http://jocaml.inria.fr/) (concurrent and distributed programming)
- [Real World OCaml](http://realworldocaml.org/)
- [Python](http://www.python.org/) (and
  [documentation](http://docs.python.org/))
- [PyMC](http://pymc-devs.github.io/pymc/) and [Bayesian Methods for
  Hackers](http://camdavidsonpilon.github.io/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/)
- [Real World Haskell](http://book.realworldhaskell.org/)
- [Learn You A Haskell](http://learnyouahaskell.com/)
- [What I Wish I Knew When Learning Haskell 2.0](http://dev.stephendiehl.com/hask)
- [Write Yourself a Scheme in 48 hours](http://en.wikibooks.org/wiki/Write_Yourself_a_Scheme_in_48_Hours)
- [Learn Prolog Now](http://www.learnprolognow.org/)
- [Mercury](http://www.mercurylang.org/)
- [Monad](http://blog.jcoglan.com/2011/03/05/translation-from-haskell-to-javascript-of-selected-portions-of-the-best-introduction-to-monads-ive-ever-read/)
  [tutorials](http://blog.sigfpe.com/2006/08/you-could-have-invented-monads-and.html)
- [Macros in Racket](http://www.greghendershott.com/fear-of-macros/index.html)
- [Functional programming book reviews](http://alexott.net/en/fp/books/)
- [Fortran](http://en.wikipedia.org/wiki/Fortran_95_language_features)
  [standards](http://fortran90.org/),
  [practices](https://bitbucket.org/eric_t/modern-fortran/wiki/Home),
  [examples](http://flibs.sourceforge.net/examples_modern_fortran.html) and
  [compiler support](http://gcc.gnu.org/wiki/GFortran)

### Type Systems

- [Coq](http://coq.inria.fr/)
- [Agda](http://wiki.portal.chalmers.se/agda/)
- [Certified Programming with Dependent Types](http://adam.chlipala.net/cpdt/)
- [Software Foundations](http://www.cis.upenn.edu/~bcpierce/sf/)
- [Homotopy Type Theory](http://homotopytypetheory.org/book/)
