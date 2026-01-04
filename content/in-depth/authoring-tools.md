+++
title = "Authoring Tools"

[extra]
section = "In-Depth Guides"
+++

Tools for **authoring** are ones that help you create publishable documentation
materials, often by processing some set of input **documentation source** files.
In the modern documentation landscape, this almost always means tools that
generate **HTML**, since software documentation is almost always delivered as a
website.

The aim of this guide is to help you select an appropriate authoring tool, or
tools, for your project. Authoring tools may or may not integrate with
**[publishing tools](@/in-depth/publishing-tools.md)**, which are responsible
for making the generated content publicly available. For instance, if your
authoring tool generates a static HTML website, you’ll have [numerous
options][static] for choosing how to publish your content. Platforms like
[GitBook], on the other hand, generally meld authoring and publishing
functionalities.

[static]: https://github.com/awesomelistsio/awesome-static-website-services#readme
[GitBook]: https://www.gitbook.com/


# Language-Specific Tools

Popular tools for software documentation are usually tightly associated with
specific programming languages, because when most people think of “software
documentation” they leap to “API reference material,“ and API references almost
always need to be created through language-specific tooling. One of the goals of
One Good Tutorial, however, is to underline (taking inspiration from [the
Diátaxis system][dtx]) that an API reference is just one element of good-quality
documentation, and in many ways is far from the most important element at that.

That being said:

1. Most API documentation tools are able to embed that material in a
   superstructure that’s suitable for expressing all items on [the One Good
   Tutorial checklist][cl].
1. API reference material is likely to be the element of your documentation
   that’s the most challenging to format and render.

[dtx]: https://diataxis.fr/
[cl]: ../..

So, to first order, if your project exposes an API in a particular language
(say, [Rust]), you should probably use that language’s preferred documentation
tool ([Rustdoc]) if one exists. The main reason to reconsider would be if you
know that your documentation will need to include other challenging forms of
content (e.g., interactive [Jupyter] notebooks) that the language-specific tool
can’t handle.

[Rust]: https://rust-lang.org/
[Rustdoc]: https://doc.rust-lang.org/rustdoc/what-is-rustdoc.html
[Jupyter]: https://jupyter.org/


# Example: README.md

Code-hosting services like [GitHub] generally populate repository landing pages
with the contents of a `README.md` [Markdown] file if one exists. It is entirely
reasonable for some projects to deliver all of their documentation through a
single `README.md` file.

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

If your project provides one or more APIs, a single Markdown file probably won’t
do the job. (In [ai/size-limit], there is a “JS API” section, but it’s minimal.)
In that case, your `README.md` should be relatively terse and focus on topics of
interest to developers. Such a README should mainly link to your primary
documentation, but you should reproduce key information ([install
instructions][install], [legal statement][legal]) if it’s not in danger of
getting out-of-date.

[install]: @/in-depth/installation-instructions.md
[legal]: @/in-depth/licensing-statements.md

## Additional Resources

- [GitHub Markdown: Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [CommonMark.org](https://commonmark.org/) — formalized Markdown specification
- [matiassingers/awesome-readme: A curated list of awesome READMEs](https://github.com/matiassingers/awesome-readme#readme)


# Hierarchical Static Sites

Many, many documentation tools ultimately produce output in the form of some
kind of **hierarchical static site**. That is:

- The output is a tree of web content files: HTML, CSS, JavaScript, etc.
- The content is conceptually organized in a tree-like hierarchy that
  maps onto a URL path structure.

Such content is extremely portable and comes with a huge number of options for
[hosting locally][oneliners] or [publicly][static].

[oneliners]: https://gist.github.com/willurd/5720255


# Example: Python with Sphinx

[Sphinx] is the dominant documentation tool for Python projects. It has
competitors (chiefly [MkDocs] as of this writing), but is still probably the
safest choice for a basic Python project documentation tool.

[Sphinx]: https://www.sphinx-doc.org/
[MkDocs]: https://www.mkdocs.org/

Like many such tools, Sphinx ultimately emits a **static HTML website**
with predominantly **hierarchical** organization:

```
* Landing Page
|-- Installation Instructions
|-- Tutorials
| |-- Off-Axis Slicing
| |-- Simple Particle Plot
| |-- [...]
|-- Reference Materials
| |-- File Formats
| | |-- JSON State File Schema
| | |-- [...]
| |-- Python API
| |-- [...].
```

Sphinx supports two main documentation source formats: [reStructuredText][rst]
(ReST) and [MyST][myst], a superset of [Markdown]. ReST is older and

[rst]: https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html
[myst]: https://mystmd.org/