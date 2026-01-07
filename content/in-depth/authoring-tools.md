+++
title = "Choosing an Authoring Tool"

[extra]
section = "In-Depth Guides"
+++

Tools for **authoring** are ones that help you create publishable documentation
materials, often by processing some set of input **documentation source** files.
In the modern documentation landscape, this almost always means tools that
generate **HTML**, since software documentation is almost always delivered as a
website.

The aim of this guide is to help you select an appropriate authoring tool (or
tools) for your project. Authoring tools may or may not integrate with
**[publishing tools](@/in-depth/publishing-tools.md)**, which are responsible
for making the generated content publicly available. For instance, if your
authoring tool generates a static HTML website, you’ll have [numerous
options][static] for choosing how to publish your content. Platforms like
[GitBook], on the other hand, generally meld authoring and publishing
functionalities.

[static]: https://github.com/awesomelistsio/awesome-static-website-services#readme
[GitBook]: https://www.gitbook.com/


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
`README.md` [Markdown] file in your code repository. This is by far the easiest
option if it will meet your needs.

[Markdown]: https://en.wikipedia.org/wiki/Markdown

If neither of the above options feels right, the next option to consider is a
[static site generator][ssg] for the superstructure of your content, probably
with a lot of links to more specialized content (such as API docs, Jupyter
notebooks, videos, slideshows, etc.).

[ssg]: https://about.gitlab.com/blog/comparing-static-site-generators/

If you have a vision for your docs that doesn’t feel like it will fit into any
of the above models, there’s good news and bad news. The good news is that
anything is possible — “documentation” is just another way of saying “content,”
and there have never been more tools for creating content than now. The bad news
is that you’ll be straying off of the beaten path, so the going will be slower.


# Language-Specific Tools

Most programming languages are strongly associated with particular documentation
authoring tools. [Python] is linked with [Sphinx] and [MkDocs], Ruby with [RDoc]
and [YARD], [Rust] with [rustdoc], [TypeScript] with [typedoc], and so on.

[Python]: https://www.python.org/
[Ruby]: https://www.ruby-lang.org/
[RDoc]: https://ruby.github.io/rdoc/
[YARD]: https://yardoc.org/
[Rust]: https://rust-lang.org/
[rustdoc]: https://doc.rust-lang.org/rustdoc/what-is-rustdoc.html
[TypeScript]: https://www.typescriptlang.org/
[typedoc]: https://typedoc.org/

Why is this? The key is that for every language there’s an understandable need
to create API reference documentation, and such material is unique to each
language (by definition, the semantic structure of an API depends on the
particular details of its implementation language) and, consequently, likely to
be complex to format (basic [Markdown]-esque typesetting won’t do the job). So
virtually every language ends up having at least one bespoke documentation tool.

One of the goals of One Good Tutorial is to underline (taking inspiration from
[the Diátaxis system][dtx]) that an API reference is just one element of
good-quality documentation, and in many ways is far from the most important
element at that. But that being said:

1. Most API documentation tools are able to embed that material in a
   superstructure that’s suitable for expressing all items on [the One Good
   Tutorial checklist][cl].
1. API reference material is likely to be the element of your documentation
   that’s the most challenging to format and render.

[dtx]: https://diataxis.fr/
[cl]: ../..

So, in many cases, you can do everything you need within your language-specific
documentation tool.


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
- Furthermore, the content is conceptually organized in a tree-like page
  hierarchy as well.

This kind of output is called *static* in contrast with more complex, dynamic
web apps that involve custom webserver code. Static content is extremely
portable and can be published using virtually any generic webserver; there are
literally [dozens of options][oneliners].

[oneliners]: https://gist.github.com/willurd/5720255

An hierarchical content organization for software documentation might look like
this (in part):

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
| |-- [...]
```

Most of us are very familiar with this approach to organizing content, but it’s
not inevitable. For instance, Wikipedia doesn’t have this structure; instead,
it’s basically a giant “bag” of millions of articles, with no particular
ordering or organizational structure imposed on them.


# Example: Python with Sphinx

[Sphinx] is the dominant documentation tool for Python projects. Its output
takes the form of an hierarchical static site.

(For the record: Sphinx and many other documentation tools can generate output
in other formats like PDF as well. Except in special circumstances, you should
focus all of your effort on the web/HTML manifestation of your documentation. It
is by far the most convenient for most users, it is what will be indexed by
search engines, and modern browsers can accomplish any effect that you can
possibly dream up.)

Sphinx has competitors (chiefly [MkDocs] as of this writing), but is still
probably the safest choice for a basic Python project documentation tool.

[Sphinx]: https://www.sphinx-doc.org/
[MkDocs]: https://www.mkdocs.org/

Sphinx supports two main documentation source formats: [reStructuredText][rst]
(ReST) and [MyST][myst], a superset of [Markdown]. ReST is older and

[rst]: https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html
[myst]: https://mystmd.org/