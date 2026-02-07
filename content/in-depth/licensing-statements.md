+++
title = "Licensing Statements"
description = """\
  How to prepare a licensing statement for your scientific software’s \
  documentation. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

A **licensing statement** informs users about the legal status of your code.

It may seem annoying and tedious to have to write up this information, and we
can’t honestly claim that it isn’t. But it’s important: formally, people aren’t
even allowed to download your software if you don’t provide the right
information. The good news is that in most cases, you only need to include a few
boilerplate sentences in the end — see the examples below. But you should
understand what those sentences mean.


# A Brief Primer on Copyright Law

*Disclaimer: we are not lawyers, this is not legal advice, yadda yadda yadda.
Don’t make any important decisions without talking to an actual expert.*

You need to provide a licensing statement with your software because any
nontrivial source code is presumed to be copyrighted intellectual property (IP).
The default stance of US ([and international][berne]) copyright law is that if
you get your hands on a copyrighted work, you’re not allowed to duplicate it.
This applies not only to, say, photocopying printed books, but also to the mere
act of downloading or copying a digital file. So, in principle, even if I can
trivially find your source code on GitHub, legally speaking I shouldn’t assume
that I'm allowed to do anything with it besides look at it.

[berne]: https://en.wikipedia.org/wiki/Berne_Convention

**Licensing** is how the owner of a copyrighted work grants other people
additional rights vis-à-vis that work. By attaching a license to your code, you
can allow people to, well, actually download it and use it at all. This is why
software licensing is such a big deal!

But who owns a copyrighted work, anyway? The person who created it, you might
think. And that’s often true. But if you created something as part of your job,
your employer probably gets ownership. *This point is highly relevant to
scientific software!* Virtually every university and lab will have policies, and
often an entire office, devoted to managing the intellectual property created by
its employees. If you're writing software at work, you should spend an hour
“eating your spinach” and understanding your employer’s policies.

There’s no magical central database of copyright owners, so it’s also important
to provide a **copyright statement** with your software identifying its legal
owner. This is the classic “Copyright {Year} {Name}” language that you see
everywhere. If you don’t provide this information, work easily becomes
“orphaned”: a future lawyer looking at your software might conclude that one
simply can’t be sure who actually owns it anymore. Without that knowledge, you
can’t modify or even rigorously verify the licensing terms.

There’s one more wrinkle worth mentioning: a work “prepared by an officer or
employee of the United States Government as part of that person's official
duties” is not eligible for copyright, and is instead part of the **public
domain** ([with nuances][usg]). It’s not copyrighted intellectual property; it’s
just data. People can duplicate it to their heart’s delight without worrying
about licenses or anything else. The documentation of public-domain software
should still include a legal statement, though, to make its public-domain status
explicit (see below).

[usg]: https://en.wikipedia.org/wiki/Copyright_status_of_works_by_the_federal_government_of_the_United_States


# Choosing a License: The IP-Centered Approach to Open Source Software

The pioneers of the Free Software movement had a brilliant insight: they could
unleash a huge amount of creativity by creating a *standard license* that
enshrined their values. The [GNU General Public License][gpl] (GPL) says that
anyone can examine and use the attached source code, but that anything that they
build using the code must *also* be made available under the same terms. (Hence
its description as a “viral” license.) This is an exceedingly clever tactic
because it promotes the creation of a coherent free software commons without
requiring individual developers to hire lawyers, fully understand the legal
angle, or coordinate in any way. Just slap the GPL on your code and you’re
contributing.

[gpl]: https://www.gnu.org/licenses/licenses.html#GPL

Fundamentally, this approach that centers the fact that software is intellectual
property — *which is true whether you want it to be or not.* In the IP paradigm,
the license is everything. And for several decades, the world of free and
open-source software was pervaded by, shall we say, vigorous debates over the
merits of different licensing schemes — there are [literally dozens][osil] to
choose from. Choosing a license is necessary, but it unavoidably ties you to
a position in these debates.

[osil]: https://opensource.org/licenses

Therefore, although we are not at all eager to rekindle any flamewars, One Good
Tutorial must dive into a bit more detail. At a minimum, you should be aware of
some of the terminological subtleties. When people talk about **free software**,
they usually mean something with a viral-type license — here “free” is in the
sense of “free speech”, not “zero cost”. When people talk about **open-source
software**, they may intentionally be referring to the pool of software that is
open-source but not licensed under viral terms — which is much more palatable to
corporate interests. From a certain perspective, free is a subset of open, and
you’ll see some people refer to “F/OSS” or “FLOSS” (Free / [Libre] / Open-Source
Software) in an effort to bring everyone under one umbrella. But the people who
care about capital-F Free software will object that stringency of their
licensing terms is the *essence* of their project.

These days, you may see less clarity on the distinction above because the honest
truth is that to a good approximation, [the open-source-but-not-Free approach
has won][licpop]. Many younger developers have never been subjected to endless
email back-and-forths about “free versus open” and don’t fully understand the
ideological underpinnings of the distinction. There are downsides to that, but
you won’t find many people wishing for the flamewars to come back.

[licpop]: https://opensource.org/blog/the-most-popular-licenses-for-each-language-2023

The Free Software camp is more explicitly ideological and also more centralized.
Adopting the GPL involves some level of entanglement with the [Free Software
Foundation][fsf] (FSF), which controls the GPL and encourages you to [transfer
the ownership of your software’s copyright to them][fsfxfer]. (This is not an
outlandish thing to ask; you may be familiar with copyright transfer forms when
publishing scholarly articles. The motivation is that a dedicated organization
with actual lawyers can do a better job of managing and defending a portfolio of
intellectual property than you, a random private individual.) The FSF has also
[been criticized][fsfcrit] for both its tactics and its tight association with
its founder, Richard Stallman, who has made [controversional comments about
the Jeffrey Epstein scandal][rmsje].

[fsf]: https://www.fsf.org/
[fsfxfer]: https://www.fsf.org/bulletin/2022/fall/copyright-assignment-with-the-fsf
[fsfcrit]: https://en.wikipedia.org/wiki/Free_Software_Foundation#Criticism
[rmsje]: https://en.wikipedia.org/wiki/Richard_Stallman#Comments_about_Jeffrey_Epstein_scandal


# Example: The MIT License

The [MIT License][mit] is one of the most popular open source licenses. It has
the benefit of being quite short — around 160 words. If you cannot wait to move
onto the next topic and stop reading about copyright law, read it — if the text
seems reasonable to you, it’s a fine choice. Here it is:

[mit]: https://opensource.org/license/mit

> Copyright **{COPYRIGHT HOLDER}**
>
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the “Software”), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.

You should include the full text of the license with your source code,
traditionally in a file called `LICENSE`, but it’s overkill to include it in
your documentation. The legal statement in your documentation might read:

> ## Legal Statement
>
> The software is licensed under [the MIT License][mit]. Copyright **{Copyright Holder}**.

Note that the standard license text includes a template copyright statement,
which should be filled in with the right information. It is *very easy* to
forget to update this information. You should also make sure that your `LICENSE`
file included in any source code packages that are derived from your repository
as well.

The traditional advice is to include a full copyright and licensing statement in
every single source file in your codebase. That gets to be a hassle quickly,
especially if your copyright statement includes the copyright year, which you
are recommended to update to include every year in which the given file is
modified. It is probably fine to standardize on a much more minimal statement:

> Copyright **{Copyright Holder}**. Licensed under the MIT License.

[Copyright statements without the year are common][noyear], and there’s no
realistic ambiguity about what one means about "the MIT License".

[noyear]: https://daniel.haxx.se/blog/2023/01/08/copyright-without-years/


# Counterexample: All Rights Reserved

While your legal statement should mention copyright ownership, some people
reflexively follow their copyright statement with:

> ## Legalities [DO NOT DO THIS:]
>
> Copyright **{Year}** **{Your Name}**. All rights reserved.

Do **not** do this. “All rights reserved” is a kind of anti-license, meaning
that you are not granting anyone any rights to do anything at all with your
copyrighted work! Just don’t write those three words.


# Counterexample: “Fun” Licensing

Some people also make up their own license language, sometimes just in an
attempt to be fun, sometimes with a purpose. For instance, [the JSON
license][jsonl] is the MIT license plus a statement: “The Software shall be used
for Good, not Evil.” This has led to actual legal problems involved in the
adoption of the standard.

[jsonl]: https://www.json.org/license.html

You know what’s actually fun? Creating software that has a tangible impact on
the world; also, not having to pay lawyers. Nonstandard licensing language will
only get in the way of these. If you are truly committed to a custom license,
OK; otherwise, if you’re tempted to do anything inventive when it comes to
licensing, find literally any other way to express yourself instead.


# Other Licenses

If you care to keep digging, you can find lots of discussion comparing the MIT
license with other major options like [Apache 2.0], [ISC], or [BSD], as well as
the GPL. Any search engine will turn up dozens. Here are a few:

[Apache 2.0]: https://opensource.org/license/apache-2-0
[ISC]: https://opensource.org/license/isc-license-txt
[BSD]: https://opensource.org/license/bsd-3-clause

- [choosealicense.com](https://choosealicense.com/)
- [Codecademy: Choosing an open source license](https://www.codecademy.com/article/choosing-an-open-source-license)
- [Carnegie Mellon University: Open source license comparison grid](https://www.cmu.edu/cttec/forms/opensourcelicensegridv1.pdf) (PDF)

It may be advantageous — sometimes, necessary — to choose a license that aligns
with other software that your code depends on or otherwise interacts with. This
is a topic known as [license compatiblity][compat].

[compat]: https://en.wikipedia.org/wiki/License_compatibility


# Example: Public Domain

Even if you’re not an employee of the US Federal government, you might be able
to explicitly dedicate your work to the public domain. The “might” here is
because if your code is written at work, your employer may well have an opinion
on the matter.

[The Unlicense][unl] is a template for disclaiming copyright interest in your
code. The website also includes a variety of material discussing why you might
wish to do so.

[unl]: https://unlicense.org/


# Multiple Licenses

There’s no reason you can’t offer up the same source code under multiple
licenses. This is basically saying: “you can use this code under either these
terms, *or* these other terms”. In some communities this is common. For
instance, many [Rust] packages are dual-licensed under both MIT and Apache-2.0.

[Rust]: https://rust-lang.org/


# Licensing Documentation and Other Non-Code Elements

You might also wish to make different pieces of one project available under
different licenses. In particular, licenses that are meant for *code* may not
apply well to *text*, and your software’s documentation is almost surely a
copyrightable work in its own right.

It’s common for projects to distribute all of their materials under a single
code license, and in most cases that’s fine. But if you want, there are
standardized licenses for non-code works that you can choose from, chiefly:

- [Creative Commons license family](https://creativecommons.org/share-your-work/cclicenses/)
- [GNU Free Documentation License](https://www.gnu.org/licenses/fdl-1.3.html)

For instance, you may have noted that the One Good Tutorial material
is licensed under the Creative Commons [CC BY-SA 4.0][ccbysa4] License.

[ccbysa4]: https://creativecommons.org/licenses/by-sa/4.0/

It may be most important to think about this angle if your software includes
significant data or art assets. These are *also* copyrightable materials, and
you may want or need to distribute them under specific licenses.
