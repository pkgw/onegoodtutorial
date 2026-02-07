+++
title = "Contact Information"
description = """\
  How to include contact information in your scientific software’s \
  documentation. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

**Contact information** tells the users of your software how to start a
conversation with the people responsible for the project.

This documentation element can be extremely short, and need not live on its own
page. But it’s important to provide clear contact information to offer a path
forward for the times when your users have questions that your written
documentation doesn’t quite answer. Once the coding is done, one of the most
important things you can do to help your project’s success is to establish a
reputation that questions will be answered helpfully and promptly. (The other
major thing being to provide [a high-quality
tutorial](@/in-depth/tutorial-planning.md), of course!)


# Example: Individual Email

If there is an individual who is the clear best contact point for the project,
it is probably best to direct users to that person’s email address.

> ## Getting in Touch
>
> If you have questions or feedback, reach out to [Peter K. G. Williams][pkgw].
> His email address is [pwilliams@cfa.harvard.edu][pkgwemail].

[pkgw]: https://newton.cx/~peter/about-me/#contact
[pkgwemail]: mailto:pwilliams@cfa.harvard.edu

If that person has a website, preferably with a distinct Contact page, a link to
it provides redundancy.

In the modern internet, there’s no point to obscuring the email address with
`[NOSPAM]` and the like — the address is guaranteed to already be in spammers’
databases: if not from a public source, then from one of the data breaches that
happen across the commercial web every day. Make your users’ lives easier by
just giving them the real, actual email address.


# The dual purpose of contact information

The primary purpose of this documentation element is ­to serve users who have
questions — **support**. Your documentation can’t possible cover all questions
that your users will have, so you want to make it as blazingly obvious how
to get help when it’s needed. And the kind of help that people prefer above
all others is help from a person.

An important additional purpose of this documentation element, however, is to
identify who’s in charge — to allow people to **contact leadership**. This is
especially relevant for scientific software where current or potential users
might need to reach out with inquiries about formalizing collaborations, grant
proposals, and so on. (Ironically, while the *product* of scientific research is
ideally public and impersonal, its *conduct* is often very much the opposite.)

Although your contact information section will likely list one or more people’s
names, it is not the purpose of this section to give credit for the creation of
the software. This is better served by the author list associated with your
project’s [citation metadata](@/in-depth/software-citation.md). Therefore, your
contact information should be minimal and focused on the above two needs;
providing an extensive list of names will only muddle things.

For new projects, a single documentation element can meet both of these needs
because the lists of relevant individuals are likely to be identical, or nearly
so. But once a project reaches a sufficient scale, this element may need to
bifurcate. If your project has acquired a robust user community, it has probably
reached the point where your documentation should have a “Support” section, and
you will be well-served to direct support questions to community forums rather
than to project leadership. Meanwhile, for the reasons given above, it still
remains important to provide a “Contact Information” section that identifies
who’s in charge.


# Example: Issue Tracker

If your project’s source code is hosted on a platform like [GitHub] that comes
with an associated issue tracker (e.g., [GitHub Issues][ghi]), you may wish to
direct people there:

[GitHub]: https://github.com/
[ghi]: https://github.com/features/issues

> ## Contact Information
>
> To report bugs, ask questions, or offer feedback, please file an issue on [the
> project’s issue tracker on GitHub][ghex]. This is the correct place to go even
> for general questions (i.e., things that aren’t bug reports).
>
> For project-level inquiries, reach out to [Peter K. G. Williams][pkgw] at
> [pwilliams@cfa.harvard.edu][pkgwemail].

[ghex]: https://github.com/pkgw/onegoodtutorial/issues/new

This approach favors the “support” role of the contact information element.
There are advantages to its impersonal nature: the guidance will remain valid
even if the project leadership evolves over time, and interactions result in a
public documentation trail. On the other hand, some users may not have existing
accounts on your code-hosting platform (consider your
[personas](@/in-depth/personas.md)), and even those that do may not feel
comfortable using the issue tracker for generic support questions. If your issue
tracker has a notion of [“issue templates”][ghit], set up a few that make it
clear that it’s appropriate to use the tracker for things other than bug
reports.

[ghit]: https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates

Given an issue tracker link, savvy and/or determined users will be able to infer
the identity of your project leadership. But why make things hard on people? If
your primary contact mechanism is a public or depersonalized channel like an
issue tracker, you’re encouraged to document a private contact channel as well.
This is more equitable for people who don’t already know the project team
personally.


# Case Study: Bioconductor

For larger projects, the notion of “contact information“ starts becoming
somewhat ill-defined. The problem becomes that there are *too many*
communications channels out there, all of which are potentially ways to contact
someone about the project. For instance, as of this writing, the [Bioconductor]
homepage lists the following:

[Bioconductor]: https://www.bioconductor.org/

> ## Connect With the Community
> - [Support Forums](https://www.bioconductor.org/help/support/) [uses [custom forum software!](https://support.bioconductor.org/info/about/)]
> - [Community Blog](https://bioconductor.github.io/biocblog)
> - [YouTube Channel](https://www.youtube.com/user/bioconductor)
> - [Community Chat](https://chat.bioconductor.org/) [uses [Zulip](https://zulip.com/)]
> - [LinkedIn](https://www.linkedin.com/company/bioconductor/)
> - [Bluesky](https://bsky.app/profile/bioconductor.bsky.social)
> - [Mastodon](https://genomic.social/@bioconductor)
> - [F1000 Research Channel](http://f1000research.com/channels/bioconductor)
> - [Publications](https://www.bioconductor.org/help/publications/)
> - [Bioconductor Related Events](https://www.bioconductor.org/help/events/)
> - [Bioconductor Seminar Series](https://www.bioconductor.org/help/seminar-series/)

The unfortunate thing is that *you can’t control what communications channels
your project needs to use*. If people start posting questions about your project
on StackExchange, it’s strongly in your interest to start monitoring and
answering them there, even if you’d rather not add yet another discussion venue
to the mix. Between that and the fact that “place for people to communicate with
each other” is a kind of website that’s launched every day, popular projects
should expect to constantly be shifting communications across different
platforms, as a simple fact of life.

When it comes to documentating project communication channels, it can be helpful
to focus on users’ needs. These can be sorted into a few broad bins, such as:

- I have a question
- I want to get involved
- I want to know what’s new
- I want to talk to the people in charge

You can’t prevent people from using whichever communications channel they
stumble upon. The best you can do, then, is offer them clear guidance: “If you
have a question, go to the forum. If you want to get involved, introduce
yourself on the Zulip instance. If you want to know what’s new, follow our
Bluesky account. If you want to talk to leadership, send an email to `xxx@yyy`.”
People will still tweet support questions at the Bluesky account, but there’s
literally nothing you can do to prevent that.


# Additional Resources

- [The Good Docs Project: Contact Support template guide](https://www.thegooddocsproject.dev/template/contact-support)
- [The Good Docs Project: Our Team template guide](https://www.thegooddocsproject.dev/template/our-team)
