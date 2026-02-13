+++
title = "About One Good Tutorial"
description = """\
  One Good Tutorial is a resource for people who are documenting scientific \
  software. It provides a checklist that defines a “minimum viable \
  documentation product” for scientific software projects, a playbook for preparing \
  checklist-compliant documentation from scratch, and a set of supporting in-depth \
  guides.\
"""

[extra]
section = "About"
+++

[**One Good Tutorial**](https://onegoodtutorial.org/) is an instructional resource for people
who are documenting scientific software. The main idea is right there in the
name: the most important thing is that your software’s documentation includes
*one good tutorial*. You need a bit more than that, but not much more: the [One
Good Tutorial software documentation checklist](https://onegoodtutorial.org/)
defines nine core elements of scientific software documentation. The resource
also includes [a playbook](https://onegoodtutorial.org/playbook/) you can follow
to prepare these nine elements with a minimum of angst and a number of
supporting [in-depth guides](https://onegoodtutorial.org/in-depth/).

One Good Tutorial was developed by [Peter K. G.
Williams][pkgw] with the support of a [Better Scientific
Software Fellowship](https://bssw.io/pages/bssw-fellowship-program).

[pkgw]: https://newton.cx/~peter/


# Getting in Touch & Feedback

To report issues or propose improvements to One Good Tutorial, you are invited
to start a conversation by filing [an issue][ghissue] or [a pull request][ghpr]
on the One Good Tutorial source code repository on GitHub.

[ghissue]: https://github.com/pkgw/onegoodtutorial/issues/new
[ghpr]: https://github.com/pkgw/onegoodtutorial/pulls

The BSSw team would like to collect feedback about the user impact of this
resource. Please consider [taking this three-minute
survey](https://www.surveymonkey.com/r/FDDF2ZW) if you have anything you’d like
to convey; you can specify whether you’d like this feedback to be shared with
the author, or not.

To reach out to the author directly, or for any other needs, contact him at
<pwilliams@cfa.harvard.edu>.


# Citing or Acknowledging One Good Tutorial

If you found this resource useful during the preparation of your software’s
documentation, you are encouraged — but not obligated — to mention it in your
[acknowledgments](@/in-depth/acknowledgments.md) section. A suggested statement is:

> These materials were initially prepared following version
> {{ checklist_version() }} of the [One Good Tutorial software
> documentation checklist][self].

[self]: https://onegoodtutorial.org/

If you discuss One Good Tutorial in a scholarly context, you should cite it. You
are reading version 0.11.0 and its DOI is
[10.5281/zenodo.18635124][vdoi]. Cite it with a BibTeX entry
like this:

[vdoi]: https://doi.org/10.5281/zenodo.18635124

```bibtex
@misc{onegoodtutorial0.11.0,
  author       = {Williams, Peter K. G.},
  title        = {One Good Tutorial (version 0.11.0)},
  year         = 2026,
  publisher    = {Zenodo},
  version      = {0.11.0},
  doi          = {10.5281/zenodo.18635124},
  url          = {https://doi.org/10.5281/zenodo.18635124}
}
```

(You may need to tweak the BibTeX content to get the correct citation text for
your particular publication venue — this is fine.) See the “Export” section of
[the Zenodo page][vdoi] for additional formats.

Another, less-formal way to acknowledge One Good Tutorial is to [add a
compliance badge](@/badge/index.md) to your project README or another
appropriate page.

# Contributing to One Good Tutorial

Your contributions are most welcome! Start by exploring [the One Good Tutorial
source code repository on GitHub](https://github.com/pkgw/onegoodtutorial/),
where you can file [an issue][ghissue] or [a pull request][ghpr]. Or if you’re
not sure exactly where to start, go ahead and [get in
touch](#getting-in-touch-feedback) with the author.

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
