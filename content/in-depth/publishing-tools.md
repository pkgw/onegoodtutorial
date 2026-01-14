+++
title = "Choosing a Publishing Tool"

[extra]
section = "In-Depth Guides"
+++

Tools for **publishing** documentation are ones that make your materials
publicly available in some fashion. In the modern documentation landscape, this
almost always means tools that set up websites, since that’s how software
documentation is almost always delivered. The aim of this guide is to help you
select an appropriate publishing tool (or tools) for your project.

Publishing tools may or may not integrate with **[authoring
tools](@/in-depth/authoring-tools.md)**, which help you create your publishable
materials in the first place. For instance, the [docs.rs] service automatically
publishes documentation for any public [Rust] crate that includes [rustdoc]
source files in the standard configuration. Regardless of the tightness of any
such integration, your choice of publishing tool(s) will likely be strongly
influenced by your choice of authoring tool(s).

[docs.rs]: https://docs.rs/
[Rust]: https://rust-lang.org/
[rustdoc]: https://doc.rust-lang.org/rustdoc/what-is-rustdoc.html

If you author your documentation using a **[docs as code][dac]** approach, in
which your project’s documentation source lives in the same repository as its
source code, it is extremely convenient to automate docs publishing as part of
your continuous integration and deployment (CI/CD) processes.

[dac]: https://www.writethedocs.org/guide/docs-as-code/


## Executive Summary

If you’re authoring your documentation using the standard documentation tool
associated with your software’s implementation language, it may pair with a
consensus standard publishing tool you should use if feasible. For Python, the
dominant choice is to use the [ReadTheDocs][rtd] service.

[rtd]: https://about.readthedocs.com/

If you’re not aware of such a pairing, you almost surely need to publish your
docs using a “static site” hosting service. There are numerous free options
available. Ones integrated with code-hosting services such as [GitHub
Pages][ghp] or [GitLab Pages][glp] may be the most convenient.

[ghp]: https://pages.github.com/
[glp]: https://docs.gitlab.com/user/project/pages/

Unless you know that you have unusual needs, it is extremely likely that one of
the above options will work for you. Note that virtually all of these publishing
services support **custom domains** so that, with a relatively small amount of
effort, your docs can be accessed via a branded URL like
`https://docs.mycoolproject.org/` even as they’re hosted by the third-party
service.


## Example: ReadTheDocs and GitHub

If you use [ReadTheDocs][rtd] and [GitHub](https://github.com/), it is not
difficult to make it so that essentially all parts of your documentation
publishing workflow are automated. This is hugely convenient, and one of the
major appeals of the Docs As Code paradigm.

If you’re using different tools, fear not. In most cases, the setup will be
equally straightforward, and it should not be difficult to find the relevant
documentation with some basic web searches.
