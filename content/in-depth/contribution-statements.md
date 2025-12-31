+++
title = "Contribution Statements"

[extra]
section = "In-Depth Guides"
+++

A **contribution statement** is some text that tells users of your software how
they can contribute to your project.

While we believe that it’s important for every project’s documentation to
include a contribution statement, it can be *extremely* short, and need not live
on its own page.

If you do want or need to include a lengthier contribution statement in your
documentation, it is the kind of document that you should absolutely feel free
to copy from another project — giving appropriate credit, of course, with links
to the source(s), and editing to make sure that everything in the text aligns
with your specific situation.


# Example: Small GitHub Project

For many projects, this is entirely sufficient:

> ## Contributing
>
> Contributions to this project are welcome! If you would like to contribute
> code or an idea, please open an [issue](#) or [pull request](#) on GitHub.

… where the links should go to the appropriate pages on GitHub.

Of course, you should only use the above text if that's how you actually feel.
For what it’s worth, even if your project is quite popular, the fraction of
users that will seek to become contributors is likely to be perhaps a few
percent. Realistically, you are very unlikely to be overwhelmed with people
wanting to get involved.


# Example: Private Communication

You might also ask people to reach out to you directly:

> ## Getting Involved
>
> If you’d like to get involved in this project, email **{Your Name}**
> at **{your@email.address}**.

But we encourage the GitHub approach since it’s more public. For instance, if
one user posts a pull request to your project on GitHub, another user might see
it and chime in mentioning how the propose change would help them too. If all of
your coordination is done via private email, you lose this mechanism for
building up a sense of community among your users.


# Case Study: Astropy

The [Astropy Project][astropy] is highly successful and has attracted a large
number of contributors from across the astronomy community. As such, its website
has a prominent link to [a substantial contribution statement][apcs]. The
Astropy team takes care to point out that contributions can take many forms, not
just code:

[astropy]: https://www.astropy.org/
[apcs]: https://www.astropy.org/contribute.html

> The Astropy project is made both by and for its users, so we accept
> contributions of many kinds …
>
> - Feedback
> - Report an Issue
> - Code/docs
> - Project role
> - Affiliated package
> - Financial

While leaders of projects of all sizes should follow Astropy’s example and keep
in mind that contributions can come in many forms besides pull requests, laying
out detailed information for all of these avenues is probably overkill for
smaller projects. For better or for worse, only the largest and most successful
projects attract enough contributors where it becomes valuable to spend time
designing and implementing a good, formalized “funnel” to handle them. For most
projects, if your contribution statement has a generally encouraging tone and
provides clear information for how to reach out, your docs do enough — all of
the real work will be in how you respond to anyone that comes knocking at your
virtual door.

## Code of Conduct

Astropy also prominently links contribution with abidance by the project’s
**code of conduct** (CoC):

> We always welcome contributors who will abide by the [Astropy Community Code
> of Conduct][apcoc].

[apcoc]: https://www.astropy.org/about.html#codeofconduct

If your project has gotten enough traction to need a non-trivial contribution
statement, it almost certainly needs a Code of Conduct as well. The project
CoC should become part of its documentation, but adopting a CoC is much more
of a *social* process than a matter of *documentation*. Here are a few resources
on the topic:

- [Good Docs Project: Code of conduct template guide](https://www.thegooddocsproject.dev/template/code-of-conduct)
- [GitHub: Adding a code of conduct to your project](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project)
- [Contributor Covenant: A code of conduct for digital communities](https://www.contributor-covenant.org/)
- [Project Include: Guide to writing a code of conduct](https://projectinclude.org/writing_cocs)


# Case Study: PlasmaPy

The [PlasmaPy][plasmapy] Project has also gathered a significant community of
project contributors. Its [contribution statement][ppcs] contains some similar
elements to that of Astropy, but then links to a separate, much lengthier
[Contributor Guide][ppcg] that goes into details of PlasmaPy development
practices such as [writing tests][ppwt] or [adding changelog entries][ppcl].
(Astropy now has [a similar detailed guide][apcg] that is more focused on code
development; it appears to be evolving towards a broader conception of the
different contributions that can be made to the project.)

[apcg]: https://docs.astropy.org/en/latest/index_dev.html

This Contributor Guide probably took some effort to write, and is not something
that we would recommend for new projects. It gets into material that is much
less “copy-pasteable” than general guidance for contributors, since it details
practices that are quite project-specific. We also suspect that few potential
PlasmaPy contributors have had the patience to actually read the guide from
beginning to end. But all of that material comes in handy as project members
interact with prospective contributors: while reviewing pull requests or
answering questions, they can send links to the written guide material instead
of, say, writing up an explanation of the PlasmaPy changelog system for the
umpteenth time.

[plasmapy]: https://www.plasmapy.org/
[ppcs]: https://www.plasmapy.org/contribute/
[ppcg]: https://docs.plasmapy.org/en/latest/contributing/
[ppwt]: https://docs.plasmapy.org/en/latest/contributing/testing_guide.html#id4
[ppcl]: https://docs.plasmapy.org/en/latest/contributing/changelog_guide.html#adding-a-changelog-entry

## Imposter Syndrome Disclaimer

The PlasmaPy contribution statement also chooses to open with an “impostor
syndrome disclaimer”:

> We want your help. No, really. There may be a little voice inside your head
> that is telling you that you're not ready to be an open source contributor;
> that your skills aren't nearly good enough to contribute. What could you
> possibly offer a project like this one? We assure you - the little voice in
> your head is wrong. If you can write code at all, you can contribute code to
> open source. …

Note that, while both the PlasmaPy and Astropy contribution statements do
mention that project contributions can take many forms besides code, this
disclaimer does lead with a focus on code contributions. It might be better to
not specifically mention code at first, given the context.

The disclaimer also provides an example of how to credit reused text, since the
language is not original to PlasmaPy:

> This disclaimer was originally written by [Adrienne
> Lowe](https://github.com/adriennefriend) for a [PyCon
> talk](https://www.youtube.com/watch?v=6Uj746j9Heo), and was adapted by
> [yt](https://github.com/yt-project/yt) in their README file based on its use
> in the README file for the [MetPy project](https://github.com/Unidata/MetPy).
> It was then adapted by PlasmaPy.
