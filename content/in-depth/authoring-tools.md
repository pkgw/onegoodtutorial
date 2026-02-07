+++
title = "Choosing an Authoring Tool"
description = """\
  How to choose an authoring tool for your scientific software’s documentation. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

Tools for **authoring** are ones that help you create publishable documentation
materials. In the modern documentation landscape, this almost always means tools
that generate **HTML**, since software documentation is almost always delivered
as a website. The aim of this guide is to help you select an appropriate
authoring tool (or tools) for your project.

Authoring tools may or may not integrate with **[publishing
tools](@/in-depth/publishing-tools.md)**, which are responsible for making the
generated content publicly available. For instance, if your authoring tool
generates a static HTML website, you’ll have [numerous options][static] for
choosing how to publish your content. Platforms like [GitBook], on the other
hand, generally meld authoring and publishing functionalities.

[static]: https://github.com/awesomelistsio/awesome-static-website-services#readme
[GitBook]: https://www.gitbook.com/

You’re encouraged to adopt a tool that enables a **[docs as code][dac]**
approach, in which you manage your project’s documentation in the same
repository as its source code, keep docs updated as development proceeds, and
build and publish your docs using automated continuous integration and
deployment (CI/CD) processes. Most projects find docs-as-code to be the easiest
way to consistently deliver good-quality documentation. However, you might need
to use a different (or an additional) approach to handle complex content such as
tutorial videos, or doc-writing collaborators who aren’t comfortable using
version control. Either way, it’s important to think through the **build
workflow** that you will use to generate reviewable drafts of your project’s
documentation.

[dac]: https://www.writethedocs.org/guide/docs-as-code/


# Executive Summary

For most people and projects, the best authoring tool is probably the standard
documentation tool associated with your software’s implementation language. For
Python, your primary options are [Sphinx] or [MkDocs], both of which have their
pluses and minuses. If unsure, try Sphinx first, but give MkDocs a try if you
find Sphinx frustrating.

[Sphinx]: https://www.sphinx-doc.org/
[MkDocs]: https://www.mkdocs.org/

If your project does not have a large API surface area and you expect your docs
to be short overall, it’s totally valid to put everything into a single
**README** file in your code repository (probably in [Markdown] format). This is
by far the easiest option if it will meet your needs.

[Markdown]: https://en.wikipedia.org/wiki/Markdown

If you want to include material in your docs that isn’t practical to express in
your primary authoring tool (e.g., a video or live notebook), your best bet is
probably to author and publish that material separately, and link to or embed it
in your primary doc site.

If you want your docs to cleanly integrate a variety of kinds of media and
interactive content, or you’re dissatisfied with your language’s default
authoring tool, there’s good news and bad news. The good news is that anything
is possible — “documentation” is just another way of saying “content,” and there
have never been more tools for creating content than now. The bad news is that
you’ll be straying off of the beaten path, so the going will be slower. If you
want, you can think of [your documentation as its own full-fledged web
application][dawa], with all of the possibility and effort that statement
implies.

[dawa]: https://newton.cx/~peter/2024/digital-docs-are-web-apps/


# Easiest Option: Basic Markdown README

Code-hosting services like [GitHub] generally populate repository landing pages
with the contents of a `README.md` [Markdown] file if one exists. It is entirely
reasonable for some projects to deliver all of their documentation through a
single `README.md` file — the ultimate docs-as-code convenience.

[GitHub]: https://github.com/
[Markdown]: https://en.wikipedia.org/wiki/Markdown

For instance, [ai/size-limit] on GitHub does this. It is not scientific software
and its documentation is not designed around [the One Good Tutorial
checklist][cl], but qualitatively the documentation is thorough and appropriate
in scope for this relatively simple tool. This README also demonstrates some
of the effects that can be achieved with GitHub’s Markdown renderer, including
screenshots, syntax-highlighted code samples, and [disclosure arrows][discarr].

[ai/size-limit]: https://github.com/ai/size-limit#readme
[discarr]: https://en.wikipedia.org/wiki/Disclosure_widget

## Example: One Good Tutorial Itself

The [One Good Tutorial “About” page](@/about.md) is also a single Markdown page
that essentially serves as the project’s documentation. It omits a few elements
such as Installation Instructions that aren’t relevant.

If your project provides one or more APIs, a single Markdown file probably won’t
do the job, because API definitions usually require (or at least, benefit
significantly from) complex formatting. (In [ai/size-limit], there is a “JS API”
section, but it’s minimal.) In that case, your `README.md` should be relatively
terse and focus on topics of interest to developers. Such a README should mainly
link to your primary documentation, but you should reproduce key information
([install instructions][install], [legal statement][legal]) if it’s not in
danger of getting out-of-date.

[install]: @/in-depth/installation-instructions.md
[legal]: @/in-depth/licensing-statements.md

## Additional Markdown Resources

- [GitHub Markdown: Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [CommonMark.org](https://commonmark.org/) — formalized Markdown specification
- [matiassingers/awesome-readme: A curated list of awesome READMEs](https://github.com/matiassingers/awesome-readme#readme)


# Next Option: Language-Specific Tool

Most programming languages are strongly associated with particular documentation
authoring tools. [Python] is linked with [Sphinx] and [MkDocs], Ruby with [RDoc]
and [YARD], [Rust] with [rustdoc], [TypeScript] with [typedoc], and so on. If
one or more of these tools are relevant to your project, you should almost
surely build your docs around it.

[Python]: https://www.python.org/
[Ruby]: https://www.ruby-lang.org/
[RDoc]: https://ruby.github.io/rdoc/
[YARD]: https://yardoc.org/
[Rust]: https://rust-lang.org/
[rustdoc]: https://doc.rust-lang.org/rustdoc/what-is-rustdoc.html
[TypeScript]: https://www.typescriptlang.org/
[typedoc]: https://typedoc.org/

Why does each new language seem to get its own new documentation tool? The key
is that for every language there’s an understandable need to create API
reference documentation, and such material is unique to each language (by
definition, the semantic structure of an API depends on the particular details
of its implementation language) and, relatedly, likely to be complex to format
as well (basic [Markdown]-esque typesetting won’t do the job). And almost all of
these tools also include functionality to scan the source code in your
repository to populate the API documentation directly from code comments,
another highly language-specific piece of functionality. All of these factors
make it very likely that a new language will need to deliver a new tool for
authoring its API documentation.

One of the goals of One Good Tutorial is to underline (taking inspiration from
[the Diátaxis system][dtx]) that an API reference is just one element of
good-quality documentation, and in many ways is far from the most important
element at that. But, because API reference material is more demanding to
generate and format than most of the other elements on [the One Good Tutorial
checklist][cl], it ends up playing an outsized role in the selection of your
authoring tools.

[dtx]: https://diataxis.fr/
[cl]: ../..

## Additional Language-Specific Resources

- Python:
  - ReadTheDocs Sphinx Example: [code](https://github.com/readthedocs-examples/example-sphinx-basic), [rendered](https://example-sphinx-basic.readthedocs.io/)
  - ReadTheDocs MkDocs Example: [code](https://github.com/readthedocs-examples/example-mkdocs-basic), [rendered](https://example-mkdocs-basic.readthedocs.io/)
  - [Sphinx Documentation: Build your first project](https://www.sphinx-doc.org/en/master/tutorial/index.html)
  - [Sphinx Documentation: Examples](https://www.sphinx-doc.org/en/master/examples.html) (serves as a theme gallery)
  - [MkDocs Documentation: Getting Started](https://www.mkdocs.org/getting-started/)
- [C/C++ (and others): doxygen](https://www.doxygen.nl/)
- [Go: Godoc](https://go.dev/blog/godoc)
- [Java: Javadoc](https://www.oracle.com/java/technologies/javase/javadoc-tool.html)
- [R: roxygen2](https://roxygen2.r-lib.org/)
- [Ruby: RDoc](https://ruby.github.io/rdoc/)
- [Rust: rustdoc](https://doc.rust-lang.org/rustdoc/what-is-rustdoc.html)
- [TypeScript: typedoc](https://typedoc.org/)


# Integrating Other Tools

The main reason to add other tools to your documentation workflow is if there’s
a specific kind of content that you would like to include that your primary
authoring tool simply can’t handle. In such situations, the simplest way to
proceed is to leverage the power of the World Wide Web and simply cross-link
between the materials authored using different tools, but more sophisticated
approaches exist.

## Example: Video

Videos can be a perfectly legitimate form of documentation, but they‘re unlikely
to be the *primary* way in which you document your software. It is beyond the
scope of One Good Tutorial to recommend video editing or hosting options, but no
matter how you produce your video, you’re probably going to end up with an
online resource that you wish to refer to from your primary, text-driven
documentation.

The easiest way to do this is with a simple link, but most documentation tools
either have special support to embed videos, or extensions that provide such
support. For instance, the [sphinxcontrib-youtube] extension for Sphinx makes it
a one-line command to embed a video in Sphinx material.

[sphinxcontrib-youtube]: https://sphinxcontrib-youtube.readthedocs.io/en/latest/

## Example: HTML Slideshow

Empirically, slideshows are a popular form-factor for digital educational
material even when they’re not being presented live on a big screen, so you
might wish to deliver your software’s tutorial in this format. For instance,
[the One Good Tutorial playbook](@/playbook.md) is delivered as an HTML
slideshow built using the [reveal.js] framework. While it surely isn’t
*impossible* to include a [reveal.js] presentation directly into documentation
built with, say, Sphinx, most people will probably find it a lot more convenient
to author a slideshow using, say, [Google Slides] and link to it from your
Sphinx-based materials. There are some potential downsides to doing so (e.g.,
inconsistent look-and-feel of different parts of your documentation, loss of
docs-as-code purity), but in most situations these don’t outweigh the upside of
convenience.

[reveal.js]: https://revealjs.com/
[Google Slides]: https://workspace.google.com/products/slides/

## Example: Static Jupyter Notebook via Sphinx Extension

It’s also popular to use [Jupyter] notebooks for tutorials and other
code-related educational content. It’s so popular, in fact, that tools like
Sphinx have extensions to [automate the rendering of such notebooks in their
documentation builds][pynb].

[Jupyter]: https://jupyter.org/
[pynb]: https://docs.readthedocs.com/platform/latest/guides/jupyter.html

This approach can be quite convenient: you can version-control your `.ipynb`
notebook file with your code and use a pure docs-as-code workflow to publish it.
But it’s important to understand the limitations at play. Virtually all
language-specific documentation tools emit their output as **static HTML
content** — trees files containing HTML, CSS, JavaScript, etc. This output
format can accommodate a static snapshot of your notebook, [and even limited
interactivity][pynb-widgets], but can’t provide the user with the capability to
actually run code on demand. To do that would require starting up a Python
kernel for every person who visits your docs, which is *far, far* more expensive
than serving up static content.

[pynb-widgets]: https://docs.readthedocs.com/platform/latest/guides/jupyter.html#rendering-interactive-widgets

So this approach can provide authoring convenience and a familiar “look” to your
readers, but fundamentally doesn’t unlock an experience for your readers that’s
much different from reading a block of well-typeset prose. See [the docs of
PyVista][pyvd], a 3D mesh visualization package, for an example including
interactive widgets.

[pyvd]: https://docs.pyvista.org/#brief-examples

## Example: Dynamic Jupyter Notebook via MyBinder

At the other end of the notebook spectrum, there are services that truly will
host real live notebooks that allow random strangers on the Internet to run
arbitrary code. [MyBinder] is free and integrates nicely with GitHub, making it
the preferred choice in many situations. [Google Colab][colab] is another
popular option.

[MyBinder]: https://mybinder.org/
[colab]: https://colab.google/

The tradeoff is that these environments are slow to boot up, and can’t be
embedded in the rest of your docs. The [Quick Start of PyWWT][pywwtqs], an
astronomical visualization package, accepts this tradeoff because PyWWT is tuned
to operate in a [JupyterLab] environment that can be fairly complicated to set
up. The PyWWT docs encourage users to try out PyWWT inside a MyBinder
environment that’s configured to boot into a fully-prepared PyWWT+JupyterLab
environment that’s preloaded with sample notebooks.

[pywwtqs]: https://pywwt.readthedocs.io/en/stable/#quick-start
[JupyterLab]: https://jupyterlab.readthedocs.io/

## Example: Static Site Generators

While virtually all of the language-specific tools mentioned above ultimately
produce static HTML content, there are also [dozens][ssg-list], if not hundreds,
of tools that generate this kind content but aren’t associated with any
particular programming language. These are sensibly called static site
generators (SSGs).

[ssg-list]: https://jamstack.org/generators/

Many of these tools are *completely* interchangeable, but some might have
unusual capabilities that help you to create content that your primary authoring
tool has trouble with. If there’s an SSG that you use and like, it can also be a
reasonable option for documenting software that has documentation that is (1)
too complex for the everything-in-the-README approach but (2) not closely tied
to any one specific programming language. For instance, the site that you’re
reading right now fits these criteria and is generated with a tool called
[Zola].

[Zola]: https://getzola.org/

## Example: pandoc

The tool [pandoc] is described as a “universal document converter:”

[pandoc]: https://pandoc.org/

> If you need to convert files from one markup format into another, pandoc is
> your swiss-army knife.

It’s impressively capable. While pandoc is less likely to be relevant to
projects that are starting from scratch, it may be a useful part of your
documentation build workflow if you have multiple existing documentation
corpuses in different formats that you want to combine.
