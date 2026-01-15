+++
title = "Choosing a Publishing Tool"

[extra]
section = "In-Depth Guides"
+++

Tools for **publishing** documentation are ones that make your materials
publicly available in some fashion. In the modern documentation landscape, this
almost always means tools that create websites, since that’s how software
documentation is almost always delivered.

Taking an expansive view, there are many, many tools you could use to publish
your documentation — essentially as many as there are different [web hosting
services][whs]. But there are a few crowd-favorite options that will meet the
needs of the vast majority of projects. Unless you have very particular
requirements, you probably only need to consider a few choices before finding
one that will work for you.

[whs]: https://en.wikipedia.org/wiki/Web_hosting_service


# ReadTheDocs

Most open-source Python projects publish their documentation using the
[ReadTheDocs.com][rtd] service. ReadTheDocs has a free usage plan, supports any
documentation tool (not just Python-based ones), and has good integration with
continuous integration and deployment (CI/CD) services. This latter point is
very valuable if, as recommended, you embrace the **[docs as code][dac]**
paradigm.

[rtd]: https://about.readthedocs.com/
[dac]: https://www.writethedocs.org/guide/docs-as-code/

If you’re unsure whether ReadTheDocs would be a good fit for your project,
consult [its documentation][rtd] to learn more.

Note that ReadTheDocs supports **custom domains** so that, with a relatively
small amount of effort, your docs can be accessed via a branded URL like
`https://docs.mycoolproject.org/` even as they’re hosted by the third-party
service. These days, *most* publishing tools offer this feature.

## Additional Resources

- [ReadTheDocs: Tutorial](https://docs.readthedocs.com/platform/stable/tutorial/index.html)
- [ReadTheDocs: Sphinx support](https://about.readthedocs.com/tools/sphinx/)
- [ReadTheDocs: MkDocs support](https://about.readthedocs.com/tools/mkdocs/)
- [ReadTheDocs: Custom authoring tool support](https://about.readthedocs.com/tools/custom/)
- [ReadTheDocs: Git integration](https://docs.readthedocs.com/platform/stable/reference/git-integration.html)
- [ReadTheDocs: Custom domain support](https://docs.readthedocs.com/platform/stable/custom-domains.html)


# “Pages” Services

Another extremely popular option is a static website deployment service
integrated with your code host, such as [GitHub Pages][ghp] or [GitLab
Pages][glp]. While there are numerous general-purpose [static website hosting
services][sweb], these integrated options are likely to offer the easiest route
to convenient docs-as-code CI/CD integration.

[ghp]: https://pages.github.com/
[glp]: https://docs.gitlab.com/user/project/pages/
[sweb]: https://izzyreiff.github.io/awesome-static-website-hosting/

Broadly speaking, these services offer the same core features as ReadTheDocs:
support for any choice of authoring tool (but possibly more convenient support
for certain preferred tools); CI/CD integration; custom domains; and so on.

## Additional Resources

- [Sphinx Docs: Deploying via GitHub Pages](https://www.sphinx-doc.org/en/master/tutorial/deploying.html#id5)
- [Sphinx Docs: Deploying via GitLab Pages](https://www.sphinx-doc.org/en/master/tutorial/deploying.html#id6)
- [GitHub Pages: Using custom workflows with GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)
- [GitHub Pages: About custom domains and GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)
- [GitLab Pages: Getting started](https://docs.gitlab.com/user/project/pages/#getting-started)
- [GitLab Pages: Custom domains](https://docs.gitlab.com/user/project/pages/custom_domains_ssl_tls_certification/)


# Self-Hosting

We’ve highlighted the options above because they are very easy, very popular
systems for publishing documentation. But if you’re unwilling or unable to rely
on a third-party service to host your docs, it’s worth emphasizing that it is
totally possible to host them yourself. Most authoring tools produce static web
content as their output, and this is the easiest kind of content to self-host.

It’s beyond the scope of this resource to explore this topic in detail, but
if you have access to local tech experts, they can almost surely help you out.

## Additional Resources

- [AWS Hands-On Tutorials: Host a static website](https://docs.aws.amazon.com/hands-on/latest/host-static-website/host-static-website.html)
- [Netlify: Deploying a static site or single-page app](https://www.netlify.com/blog/2016/10/27/a-step-by-step-guide-deploying-a-static-site-or-single-page-app/)
