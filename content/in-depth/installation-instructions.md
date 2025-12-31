+++
title = "Installation Instructions"

[extra]
section = "In-Depth Guides"
+++

Almost every kind of software needs some form of **installation instructions**
that tell users how to load your code onto their machine.

You might be used to software that is time-consuming and tedious to install.
Perhaps you’ve created such software yourself. But we will assert: *in the
modern technology ecosystem, every piece of software can and should be easy to
install*. In most cases, your installation instructions can be just a few
sentences, and need not live on their own page.

The catch is that making your software easy to install might require a fair
amount of effort on your part — especially if you’re not familiar with modern
software packaging systems. We contend, however, that investing time in
mastering these systems is one of the best ways you can spend your time as a
developer. If you find yourself writing a long, complex set of installation
instructions, that’s a sign that you need to set off on a side quest: there’s
some kind of engineering work that has been left undone.


# Example: Basic Python Package

If your software is a typical Python package, your installation instructions
could be as short as these from
[ionize](https://lewisamarshall.github.io/ionize/):

> ## Installation
>
> One-line install using [pip](https://pypi.python.org/pypi/pip):
>
> ```sh
> pip install ionize
> ```

In many cases, there’s no need to write anything more than this. You could
consider mentioning whether your package is also available via `conda` or other
tools, but you can expect that anyone who needs it will try running `conda
install ionize` whether you write it down explicitly or not.

Virtually every modern language ([even Fortran!](https://fpm.fortran-lang.org/))
has a preferred package manager and registry supporting comparably easy installs.


# Package Manager Integration

If you want to be able to provide your users with one-line installation
instructions, you need to do some work on the backend to integrate your software
with the appropriate package manager and registry. This can be a bit of a
journey if it’s your first time undertaking such integration.

It’s beyond the scope of One Good Tutorial to tell you how to do this for your
particular software. But no matter what language you’re using, these workflows
are generally thoroughly documented and any problems you run into are
overwhelmingly likely to have Google-able answers.

## Python Hassles

Python packaging can be a bit of a pain because while there is a single
consensus Python package registry ([PyPI](https://pypi.org/)), there isn’t a
single Python project management tool: different projects might use
[setuptools], [scikit-build], [poetry], [pdm], [uv], or even something else. All
of these have their own particular workflows. Fortunately, while these tools
lead to diversity on the developer side (making packages and uploading them to
the registry), things are always consistent on the user side: `pip install` will
work.

[setuptools]: https://setuptools.pypa.io/
[scikit-build]: https://scikit-build.readthedocs.io/
[poetry]: https://python-poetry.org/
[pdm]: https://pdm-project.org/
[uv]: https://docs.astral.sh/uv/

If you need to choose which one of these Python project management tools to use,
there is unlikely to be a single best answer. As of this writing (2025), [uv]
seems to be the darling of the moment, but that could easily change. If you have
the time to comparison-shop, you might as well see if one particular tool
strikes your fancy the most. If not, there’s nothing wrong with sticking with
what you know, or what a colleague knows, or what’s used by another piece of
software that you’re familiar with.


# Example: Conda Package with Conda-Forge

The package managers that we’ve been talking about are generally strongly tied
to a single programming language. Some software might be built using multiple
languages, or need to be installed into software environments that rely on
multiple languages. In these “polyglot” cases, language-specific package
managers might not be able to accomplish what you need.

These situations used to be tricky to handle. Not anymore. These days, the
[Conda] package ecosystem has established itself the dominant framework for
easily installing polyglot software, enabling one-line install instructions
even for very complex applications:

[Conda]: https://conda.pydata.org/docs/

> ## Installation
>
> The easiest way to install **{Your Software}** is through the [Conda
> package manager](https://conda.pydata.org/docs/) with
> [conda-forge](https://conda-forge.org/):
>
> ```sh
> conda install -c conda-forge {your-package-name}
> ```

To make your software installable with Conda, someone needs to package it
into Conda’s specific file format and publish those packages. [Conda-forge]
is an impressive, fully open-source project that automates the building
and publishing of tens of thousands such packages. It is almost surely the most
convenient way to get your software into the Conda ecosystem, unless a
more field-specific framework like [Bioconda] would be appropriate.

[Conda-forge]: https://conda-forge.org/
[Bioconda]: https://bioconda.github.io/

Learning how to make Conda packages might feel like a bit of a pain, but it
remains extremely worthwhile if a language-specific package manager won’t meet
your needs.


# Case Study: daschlab

There’s a risk if you tell users to go ahead and `conda install mypackage`: if
your package is a complex application with many dependencies, and they’re
installing your software into some kind of global kitchen-sink environment,
there might be conflicts that make your package uninstallable, or even break
their environment altogether.

The [daschlab] visualization and analysis package integrates tightly with
[JupyterLab], which is often finicky to install. So its installation instructions
guide users towards installing it into its own environment, using a web-hosted
`requirements.txt` file to avoid a download step:

[daschlab]: https://dasch.cfa.harvard.edu/dr7/install-daschlab/
[JupyterLab]: https://jupyter.org/

> We strongly recommend installing *daschlab* and its dependencies using the
> popular [Conda] package management system in conjunction with the [conda-forge]
> package suite. If you need help setting up Conda or conda-forge, see [the
> official conda installation instructions][install-conda] and [how to start using
> conda-forge packages][use-cf]. There are numerous other tutorials available on
> the general internet as well.
>
> [Conda]: https://docs.conda.io/
> [conda-forge]: https://conda-forge.org/
> [install-conda]: https://conda.io/docs/user-guide/install/
> [use-cf]: https://conda-forge.org/docs/user/introduction/#how-can-i-install-packages-from-conda-forge
>
> Once these systems are set up on your computer, you can install *daschlab* by
> following running the following command in a terminal:
>
> ```sh
> conda create --name daschlab --file https://github.com/pkgw/daschlab/releases/latest/download/daschlab-conda-requirements.txt
> ```
>
> This command will produce a fair amount of output, but should not report any
> severe errors. Once the installation is complete, you can launch a new
> *daschlab* session as follows:
>
> 1. If needed, activate the daschlab environment with the command
>    ```sh
>    conda activate daschlab
>    ```
> 1. Launch JupyterLab with the command
>    ```sh
>    jupyter lab
>    ```


# Applications with `pixi`

Somewhat annoyingly, the Conda ecosystem has suffered a bit of the fragmentation
seen in Python packaging: you could also recommend that people install your
software using [mamba], or [pixi]. As in the Python case, these all pull from
the same registries, but the different tools have different strengths.

[mamba]: https://mamba.readthedocs.io/
[pixi]: https://pixi.prefix.dev/

If in doubt, you can’t go wrong recommending good old `conda`. But the `pixi`
tool is worth calling out because it has very good isolation features not
available in the other tools. (It’s also [very easy to install][pixiinst] and
quite fast.)

[pixiinst]: https://pixi.prefix.dev/dev/installation/

Instead of the named environments as used by conda (e.g., `--name daschlab` as
seen above), Pixi is workspace-based: each installed environment is associated
with a directory on disk containing a `pixi.toml` file. All of Pixi’s
environment configuration is declarative, so that you could, for instance,
manage this file using version control, and anyone tracking your changes would
have their installed environment automatically evolve to track exactly what your
file specifies.

Pixi also provides a [pack][pixipack] command that can even generate
self-extracting shell scripts that set up an entire, self-contained, conda-based
environment from a single source file. This could be useful for airgapped
deployment scenarios.

[pixipack]: https://pixi.prefix.dev/dev/deployment/pixi_pack/
