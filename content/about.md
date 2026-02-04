+++
title = "About One Good Tutorial"

[extra]
section = "About"
+++

[**One Good Tutorial**](https://onegoodtutorial.org/) is an instructional resource for people
who are documenting scientific software. The main idea is right there in the
name: the most important thing is that your software’s documentation includes
*one good tutorial*. You need a bit more than that, but not much more: the [One
Good Tutorial software documentation checklist](https://onegoodtutorial.org/)
defines eight core elements of scientific software documentation. The resource
also includes [a playbook](https://onegoodtutorial.org/playbook/) you can follow
to prepare these eight elements with a minimum of angst and a number of
supporting [in-depth guides](https://onegoodtutorial.org/in-depth/).

One Good Tutorial was developed by [Peter K. G.
Williams](https://newton.cx/~peter/) with the support of a [Better Scientific
Software Fellowship](https://bssw.io/pages/bssw-fellowship-program).


# Citing or Acknowledging One Good Tutorial

If you found this resource useful during the preparation of your software’s
documentation, you are encouraged — but not obligated — to mention it in your
acknowledgments section. A suggested statement is:

> These materials were initially prepared following version
> {{ checklist_version() }} of the [One Good Tutorial software
> documentation checklist][self].

[self]: https://onegoodtutorial.org/

If you discuss One Good Tutorial in a scholarly context, you should cite
it. You are reading version {dev} and its DOI is
[xx.xxxx/dev-build.onegoodtutorial.version][vdoi]. Cite it with the following
BibTeX entry:

[vdoi]: https://doi.org/xx.xxxx/dev-build.onegoodtutorial.version

```bibtex
@misc{onegoodtutorial{dev},
  author       = {Williams, Peter K. G.},
  title        = {onegoodtutorial {dev}},
  year         = 2026,
  publisher    = {Zenodo},
  version      = {{dev}},
  doi          = {xx.xxxx/dev-build.onegoodtutorial.version},
  url          = {https://doi.org/xx.xxxx/dev-build.onegoodtutorial.version}
}
```

See the “Export” section of [the Zenodo page][vdoi] for additional formats.


# Feedback

The BSSw team would like to collect feedback about the user impact of
this resource. Please consider [taking this three-minute
survey](https://www.surveymonkey.com/r/FDDF2ZW) if you have anything you’d like
to convey; you can specify whether you’d like this feedback to be shared with
the author, or not. To reach out to the author directly, see the next section.


# Contributing to One Good Tutorial

Your contributions are most welcome! Reach out by filing [an
issue](https://github.com/pkgw/onegoodtutorial/issues/new) or even [a pull
request](https://github.com/pkgw/onegoodtutorial/pulls) on the One Good Tutorial
source code repository on GitHub, or [contact to the author
directly](https://newton.cx/~peter/about-me/#contact).

The One Good Tutorial website is built with a static site engine called
[Zola](https://getzola.org/). To preview site changes in a local checkout of the
source code, install Zola and use the command `zola serve`.


# Changelog

You can find this project’s release notes by looking at [the `CHANGELOG.md` file
on the `release` branch of its repository][branch] or its [GitHub release
history][gh-releases].

[branch]: https://github.com/pkgw/onegoodtutorial/blob/release/CHANGELOG.md
[gh-releases]: https://github.com/pkgw/onegoodtutorial/releases


# Legalities

[One Good Tutorial](https://onegoodtutorial.org/) © 2025–2026 by [Peter K. G.
Williams](https://newton.cx/~peter/) is licensed under [CC BY-SA
4.0](https://creativecommons.org/licenses/by-sa/4.0/).


# Acknowledgments

This work was supported by the [Better Scientific Software Fellowship
Program](https://bssw.io/pages/bssw-fellowship-program), a collaborative effort
of the [U.S. Department of Energy (DOE)](https://www.energy.gov/), Office of
Advanced Scientific Computing Research via [ANL](https://www.anl.gov/) under
Contract
[DE-AC02-06CH11357](https://www.usaspending.gov/award/CONT_AWD_DEAC0206CH11357_8900_-NONE-_-NONE-)
and the National Nuclear Security Administration [Advanced Simulation and
Computing Program](https://asc.llnl.gov/) via [LLNL](https://www.llnl.gov/)
under Contract
[DE-AC52-07NA27344](https://www.usaspending.gov/award/CONT_AWD_DEAC5207NA27344_8900_-NONE-_-NONE-);
and by the [National Science Foundation (NSF)](https://www.nsf.gov/) via
[SHI](https://shinstitute.org/) under Grant No.
[2435328](https://www.nsf.gov/awardsearch/show-award?AWD_ID=2435328).