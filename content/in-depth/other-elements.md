+++
title = "Other Common Documentation Elements"
description = """\
  A list of common elements that you might wish to include in the documentation \
  of your scientific software, and discussion of when they should be used. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

[The One Good Tutorial software documentation checklist](/) specifies nine core
**documentation elements** that should be present in the docs for nearly any
piece of scientific software. There are, however, many other elements that might
make sense to include in a project’s documentation, such as:

- [Code of Conduct](#code-of-conduct)
- [Donations / Support / Sponsorship](#donations-support-sponsorship)
- [Explainers](#explainers)
- [Frequently Asked Questions (FAQ)](#frequently-asked-questions-faq)
- [Getting Help / Support](#getting-help-support)
- [How-To Guides](#how-to-guides)
- [People / Contributors](#people-contributors)
- [Quickstart / Getting Started](#quickstart-getting-started)
- [Release Notes / News / Changelog](#release-notes-news-changelog)
- [Search Functionality](#search-functionality)

The discussions below describe these elements and when you might want to add
them to your project’s documentation corpus.

The [Diátaxis system][dtx] is a helpful conceptual framework for thinking about
how to design and organize these different elements. The [Good Docs Project
template collection][gdp] includes a number of templates for some of these
documentation elements as well as others not discussed here.

[dtx]: https://diataxis.fr/
[gdp]: https://www.thegooddocsproject.dev/template


# Code of Conduct

If your project has more than a handful of users and contributors, it may need a
Code of Conduct (CoC). A CoC is a documented policy specifying how participants
in the project community should behave towards one another and how violations of
those expectations will be handled if they arise. CoCs often appear in tandem
with [contribution statements](@/in-depth/contribution-statements.md), and are
similar in that it is perfectly fine to reuse another project’s CoC if you like
it (with suitable customizations and credit to its origin, of course).

Adopting a CoC is much more of a *social* process than a matter of
*documentation*. A written CoC is not useful — in fact, it is actively
misleading ­and arguably harmful — if the resolution processes that it specifies
are not actually enforced. Many CoCs are furthermore designed for communities
sufficiently large to support an anonymous reporting mechanism and
ombudsperson-type neutral arbiter role. It is simply unrealistic to promise all
this for a small, new project with just a few participants. This is why One Good
Tutorial does not include a CoC as part of the core checklist. However, it
should go without saying that *you should not wait for your first conduct issues
to arise before your project considers formalizing a CoC*.

## Additional Resources

- Example: [Astropy Project Code of Conduct](https://www.astropy.org/code_of_conduct.html)
- [Good Docs Project: Code of conduct template guide](https://www.thegooddocsproject.dev/template/code-of-conduct)
- [GitHub: Adding a code of conduct to your project](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project)
- [Contributor Covenant: A code of conduct for digital communities](https://www.contributor-covenant.org/)
- [Project Include: Guide to writing a code of conduct](https://projectinclude.org/writing_cocs)


# Donations / Support / Sponsorship

Many non-scientific open-source software projects solicit their users for
financial contributions. Such solicitations are much rarer in the world of
scientific software, but might make sense in some cases. If you do want to ask
your users for money, be prepared to spend a lot of time figuring out if you’re
even allowed to do so, and jumping through bureaucratic hoops if so.

Note that the word “support” can be ambiguous; it might mean financial support,
or [user assistance](#getting-help-support).

## Additional Resources

- [GitHub Sponsors Program](https://github.com/open-source/sponsors)


# Explainers

In the [Diátaxis][dtx] framework, an [explainer][dtxexpl] (or explanation) is a
document that provides “context or background” for someone learning about your
software. It is not oriented towards immediate problem-solving but rather
towards helping someone become a more knowledgeable user. For example, if your
software implements a novel algorithm, you might specify it precisely in a piece
of [reference material](@/in-depth/other-elements.md), but write an explainer to
discuss *why* certain choices were made, and compare-and-contrast with prior
art.

[dtxexpl]: https://diataxis.fr/explanation/

Explainers can be some of the most rewarding, perhaps even fun (!), kinds of
documentation to read. They can be rewarding and fun to write as well. However,
they are likely to be time-consuming to write too, and realistically only a
subset of your users will actually read them. It is therefore reasonable and
acceptable if your software’s “minimum viable documentation” doesn’t include any
documents of this category. However, once you start getting questions and bug
reports from users, don’t reply to those users privately — instead, write up an
explainer answering their question, and send them to your new documentation.
(The [FAQ](#frequently-asked-questions-faq) form-factor can be convenient here.)
That way, other users with the same question (and they surely exist) can benefit
from your explanation too.

## Additional Resources

- [Diátaxis: Explanation](https://diataxis.fr/explanation/)
- [Diátaxis: The difference between reference and explanation](https://diataxis.fr/reference-explanation/)


# Frequently Asked Questions (FAQ)

FAQs have gone somewhat out of style, and not without cause. They invite
disorganization, becoming a grab-bag for information that really is useful but
ideally would be properly arranged in some sort of conceptual and functional
scheme. The page title “FAQ” tells me *nothing* about what kind of information
it might contain.

That being said, a FAQ can be a pragmatic piece of documentation from an
authoring standpoint. There are likely numerous paragraph-scale factoids about
your software that really do deserve to be documented, but in the dominant
authoring-tool paradigm where your documentation is organized as a hierarchy of
pages, it is a real, substantial friction point to figure out where in the
hierarchy each of these factoids should be slotted. The FAQ format gives you an
“escape hatch” to capture these items without having to revisit your information
hierarchy every time you add one.

One trick: if you do add a FAQ to your documentation, try to ensure that every
FAQ item is linked to from at least one other location in your documentation.


# Getting Help / Support

Your documentation should already have a section providing clear [contact
information](@/in-depth/contact-information.md). For small projects, it should
be made clear that users should get in touch with you if they need help.

Once a has grown to the point where it has a special mechanism for handling user
support requests, like a helpdesk system or special mailing list, it is likely
time to add a distinct “Getting Help” or “Support” documentation page. Some
users will know to look for systems like GitHub Issues, but not everyone, and
not everyone has a GitHub account.

Note that the word “support” can be ambiguous; it might mean help for users, or
it might mean [financial contributions](#donations-support-sponsorship).


# How-To Guides

In the [Diátaxis][dtx] framework, a [how-to guide][dtxhowto] is a document that
helps someone solve a real-world problem with your software. While superficially
similar to a tutorial, there is an important distinction. A tutorial is
fundamentally educational: it’s teaching the reader about the software, and so
might “take the long way” to illustrate an important conceptual point. A how-to
guide is fundamentally practical: it should show the reader how to achieve their
goal as straightforwardly (and tersely) as possible.

[dtxhowto]: https://diataxis.fr/how-to-guides/

The documentation for mature software should almost surely include a substantial
collection of how-to guides. And if you have the time and energy to write one or
more how-to guides for a new piece of software, so much the better. However,
when a project is just getting started, you can get away without having any — so
long as your [contact information](@/in-depth/contact-information.md) is
prominent.

Some “how-to” content might be very short, about a paragraph’s worth of
guidance. The [FAQ](#frequently-asked-questions-faq) form-factor can be a
convenient way to capture small how-tos without getting bogged down in
micromanaging the page hierarchy of your project’s documentation.

## Additional Resources

- [Diátaxis: How-to guides](https://diataxis.fr/how-to-guides/)
- [Diátaxis: The difference between a tutorial and a how-to guide](https://diataxis.fr/tutorials-how-to/)
- [The Good Docs Project: How-to Guide template guide](https://www.thegooddocsproject.dev/template/how-to)


# People / Contributors

Many projects include a page in their documentation that lists project authors
and/or personnel. For a small project, the [contact
information](@/in-depth/contact-information.md) page can serve that purpose
well. For larger projects, it can become worthwhile to document project
personnel separately, especially project leadership.

In the academic context, it is especially important that project contributors
get their fair share of credit. But, presuming that you have [made your software
citeable](@/in-depth/software-citation.md), you *already* have a way to give
credit to your contributors: by including them on the author list of the
citeable object associated with your project. It’s fair to say that these author
lists are not always scrutinized closely, but they do exist, and we ought to
take them seriously — as seriously as we take the author lists on journal
articles. This is not to say that your documentation shouldn’t include a page
listing project contributors, but that if you do create such a page, it should
preferably frame participants’ involvement in the standard academic way — as
(co-)authors of citeable objects.

## Additional Resources

- [The Good Docs Project: Our Team template guide](https://www.thegooddocsproject.dev/template/our-team)


# Quickstart / Getting Started

Some projects have dedicated “Quickstart” or “Getting Started” documentation
pages, often linked prominently from the project landing page, README, and so
on.

Your documentation should already contain freestanding [installation
instructions](@/in-depth/installation-instructions.md) and an [introductory
tutorial](@/in-depth/tutorial-planning.md), and the combination of these two
probably covers exactly the ground that a dedicated quickstart page would. If
your documentation landing page is able to include prominent links to these two
elements, a separate “Getting Started” page may not be necessary:

> ## Getting Started
>
> First [install MyGreatSoftware](#), then check out [the introductory
> tutorial](#).

(With links to the appropriate documentation pages.) A separate Quickstart page
may make sense if your software is relevant to a diverse set of audiences, in
which case you may wish to guide different people to different introductory
tutorials depending on their interests.

## Additional Resources

- [The Good Docs Project: Quickstart template guide](https://www.thegooddocsproject.dev/template/quickstart)


# Release Notes / News / Changelog

You should make releases of your software. That is, at appropriate intervals you
should lock in your code and publish it with a unique version number (and
possibly [DOI](@/in-depth/software-citation.md) as well) and tangible digital
**artifacts** (source code packages, compiled executables, etc.) that *never
change* once the release has been made. Experience has shown that users (and
software packagers) need discrete, immutable releases in order to build larger
software systems that depend on your software — and that’s something you
definitely want to encourage!

As soon as you start contemplating the *second* release of your software, you
should ensure that you have a mechanism to log “Release Notes”, a “Changelog”,
or some other equivalent journal of the changes between releases. [GitHub
Releases][ghr] and similar services have built-in places for you to document
these changes, so they may not need to be described in your project’s
documentation redundantly — you can just give a link. But if you’re not using
this kind of service, you should maintain such a journal manually in your
documentation, because users will find it *extremely* helpful to know what has
changed between one release and the next.

[ghr]: https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases

## Additional Resources

- [The Good Docs Project: Release Notes template guide](https://www.thegooddocsproject.dev/template/release-notes)


# Search Functionality

Unlike the other items mentioned in this guide, search functionality is not a
discrete element of your documentation. However, it is absolutely a feature of
your documentation that you should consider building out once your “minimum
viable product” has been unleashed upon the world.

Unless your software’s documentation suite is *very* sophisticated, it is
probably most efficient to make your documentation searchable by leveraging
general-purpose search engines that index the public internet. Regardless of
your preferred engine, you can probably find guidance about how to set up a
search box on your documentation site that uses it to search only within your
documentation site.

## Additional Resources

- [Google Programmable Search Engine][gpse] (formerly known as Google Custom Search)

[gpse]: https://programmablesearchengine.google.com/about/
