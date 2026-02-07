+++
title = "Writing a Project Synopsis"
description = """\
  How to prepare a synopsis for your scientific software’s documentation. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

A **synopsis** is a 1–3 sentence summary of your project.

Although it may not ever appear as an explicitly delineated section of your
project documentation (and certainly not its own dedicated page), it is useful
to compose an “official” project synopsis because such a summary can end up
appearing in many places: at the top of READMEs, in package manager
documentation, or even as part of grant proposals.


# Examples

The [FiPy](https://pages.nist.gov/fipy/en/latest/) project has a nice, direct
synopsis:

> FiPy is an object oriented, partial differential equation (PDE) solver,
> written in Python, based on a standard finite volume (FV) approach.

[WAFO](https://www.maths.lth.se/matstat/wafo/)’s synopsis is perhaps too terse;
the terms “waves” and “loads” could refer to lots of fields (in WAFO’s case, the
subject turns out to be oceanography):

> WAFO is a toolbox of Matlab routines for statistical analysis and simulation
> of random waves and random loads.

Here is a longer synopsis from [GemPy](https://www.gempy.org/), reproducing the
emphasis in the original text:

> GemPy is an **open-source, Python-based** project for generating **3D
> structural geological models**. Utilizing an **implicit modeling** approach,
> it enables the creation of complex combinations of **stratigraphical and
> structural features**, including folds, faults, and unconformities. Moreover,
> GemPy is specifically designed for **probabilistic modeling** to tackle
> parameter and model uncertainties effectively.

The synopsis for [Bokeh](https://bokeh.pydata.org/) makes a point of
addressing why someone might be interested in the software:

> Bokeh is an interactive visualization library that targets modern web browsers
> for presentation. Bokeh can help anyone who would like to quickly and easily
> connect powerful PyData tools to interactive plots, dashboards, and data
> applications.


# Tips

It is probably best for your synopsis to be quite matter-of-fact. It has a role
to play in marketing your work, and there is some room to try to evoke positive
feelings in your choice of language; but your best bet to draw in readers is to
make it crystal-clear what your software does. Especially in the world of
scientific software, potential users have very specific needs that they are
trying to meet, and the top question on their mind will be: does your tool meet
my needs?

That being said, it’s worth spending some time composing a good synopsis. If you
know that you’re the kind of person that can get stuck in a rabbit-hole spending
an hour debating the choice between the words “innovative” and “novel,” try
giving yourself a fixed time limit, like 15 minutes, to come up with the best
statement you can. You might not be fully satisfied with it, but call that
“version 1” and move on. If you really keep on being bothered by it after a few
days, you can always revisit.
