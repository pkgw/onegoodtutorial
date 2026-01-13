+++
title = "Other Common Documentation Elements"

[extra]
section = "In-Depth Guides"
+++

[The One Good Tutorial software documentation checklist](/) specifies eight core
**documentation elements** that should be present in the docs for nearly any
piece of scientific software. There are, however, many other elements that might
make sense to include in a project’s documentation, such as:

- [Code of Conduct](#code-of-conduct)
- [Donations / Support / Sponsorship](#donations-support-sponsorship)
- [Explainers](#explainers)
- [Frequently Asked Questions (FAQ)](#frequently-asked-questions-faq)
- [Getting Help / Support / Contact](#getting-help-support-contact)
- [How-To Guides](#how-to-guides)
- [People / Contributors](#people-contributors)
- [Quickstart / Getting Started](#quickstart-getting-started)
- [Release Notes / News](#release-notes-news)
- [Roadmap](#roadmap)
- [Search Functionality](#search-functionality)
- [Usage / Examples](#usage-examples)

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
or [user assistance](#getting-help-support-contact).

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
ought to be properly arranged in some sort of conceptual and functional scheme.
The page title “FAQ” tells me *nothing* about what kind of information it might
contain.

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


# Getting Help / Support / Contact

If it is not abundantly clear from an existing part of your software’s web
presence, you should include a documentation element telling users how to get in
touch with a human, i.e., you.

Your project probably doesn’t need a distinct “Getting Help” or “Support” page
unless it has grown to the point where it has a special mechanism for handling
user support requests, like a helpdesk system or special mailing list, that’s
distinct from a generic project bug-tracker. Tech-savvy users will know to look
for systems like GitHub Issues; other users will email you directly, no matter
how prominently you ask them to file requests using a project issue tracker.

Note that the word “support” can be ambiguous; it might help for users, or it
might mean [financial contributions](#donations-support-sponsorship).


# How-To Guides

In the [Diátaxis][dtx] framework, a [how-to guide][dtxhowto] is a document that
helps someone solve a real-world problem with your software. While superficially
similar to a tutorial, there is an important distinction. A tutorial is
fundamentally educational: it’s teaching the reader about the software, and so
might take “the long way” to illustrate a point. A how-to guide is fundamentally
practical: it should show the reader how to achieve their goal as
straightforwardly (and tersely) as possible.

[dtxhowto]: https://diataxis.fr/how-to-guides/

The documentation for mature software should almost surely include a substantial
collection of how-to guides. And if you have the time and energy to write one or
more how-to guides for a new piece of software, so much the better. However,
when a project is just getting started, you can get away without having any — so
long as your [contact information](#getting-help-support-contact) is prominent.

Some “how-to” content might be very short, about a paragraph’s worth of
guidance. The [FAQ](#frequently-asked-questions-faq) form-factor can be a
convenient way to capture small how-tos without getting bogged down in
micromanaging the page hierarchy of your project’s documentation.

## Additional Resources

- [Diátaxis: How-to guides](https://diataxis.fr/how-to-guides/)
- [Diátaxis: The difference between a tutorial and a how-to guide](https://diataxis.fr/tutorials-how-to/)
- [The Good Docs Project: How-to Guide template guide](https://www.thegooddocsproject.dev/template/how-to)


# People / Contributors

## Additional Resources

- [The Good Docs Project: Our Team template guide](https://www.thegooddocsproject.dev/template/our-team)


# Quickstart / Getting Started

## Additional Resources

- [The Good Docs Project: Quickstart template guide](https://www.thegooddocsproject.dev/template/quickstart)


# Release Notes / News


## Additional Resources

- [The Good Docs Project: Release Notes template guide](https://www.thegooddocsproject.dev/template/release-notes)


# Roadmap

# Search Functionality

# Usage / Examples
