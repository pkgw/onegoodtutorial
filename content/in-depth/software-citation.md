+++
title = "Software Citation"
description = """\
  How to prepare software citation instructions for your scientific software’s \
  documentation. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

**Citation instructions** tell users of your software what they should do to
ensure that you get proper academic credit for your work. As such, they should
be short, easy-to-follow, and prominent.

Unfortunately, the field **software citation** is a bit of a mess, in no small
part because practices vary widely between disciplines. The difficulty of
preparing citation instructions lies primarily in the difficulty of figuring out
*how to actually make your software citeable*. Once you’ve worked that out,
writing the instructions down ought to be pretty straightforward — but, well,
read on.

In a certain sense, it is beyond the scope of One Good Tutorial to try to offer
a detailed guide about how to make your software citeable. But we contend that
“citeability” is an essential feature of scientific software — and the phase at
which you’re preparing your project’s documentation is often the phase at which
you need to figure out what to do about it.


# Case Study: FiPy

In many fields, the standard practice is to publish a “regular” article about
your software, and tell users of your software to cite that separate entity,
as seen with [FiPy]:

[FiPy]: https://pages.nist.gov/fipy/en/stable/

> If you use FiPy in your research, please cite:
> [(bibtex)](https://pages.nist.gov/fipy/en/latest/_static/fipy.bib)
> [(endnote)](https://pages.nist.gov/fipy/en/latest/_static/fipy.ris):
>
> J. E. Guyer, D. Wheeler & J. A. Warren, "FiPy: Partial Differential Equations
> with Python," Computing in Science & Engineering 11(3) pp. 6—15 (2009),
> [doi:10.1109/MCSE.2009.52](http://dx.doi.org/10.1109/MCSE.2009.52),
> [http://www.ctcms.nist.gov/fipy](http://www.ctcms.nist.gov/fipy)

Many people who have strong feelings about software citation feel vehemently
that this natural-seeming approach is actually profoundly flawed, for reasons
we’ll sketch out below. But it’s certainly common. If this is the best approach
for your software, so be it.

The FiPy team tries to make citation as easy as possible by linking to BibTeX
and RiS records for users to copy-paste into their authoring tools. Some
projects go even farther and embed such records in the software itself, making
it easier to get the citation data to users *as they’re using the software*, not
just when they’re installing it.


# Example: Separate Entity, Firm Guidance

We note, however, that instructions like the above are often a bit wishy-washy:
“please cite” the following paper. If you were talking about a journal article,
you wouldn’t hedge: if someone conducting research makes use of a publication,
they are not just requested to cite it as appropriate — they are ethically
obligated to do so! Firmer language might look like:

> If you use **{Your Software}** in an academic context, cite the
> article [Author et al. (2025)](#). Its BibTeX record is:
>
> ```
> @article{ ... }
> ```


# Software Is Self-Published

You might step back and ask: why do I have to write my own citation
instructions, anyway? When you submit an article to a journal, you don’t need to
figure out how to to make that article citeable — it “just happens”. What’s the
difference with software?

In short: when you’re going through a journal, it’s the journal publisher’s job
to make sure that your article is citeable. They do this professionally, and
have created frameworks like [DOIs](https://www.doi.org/) to support that work.
Software, on the other hand, is essentially *self-published*. You have to do the
work of the publisher as well as the author, and that includes the work of
making your product citeable. This is probably *not* something that you’re an
expert in, which has the knock-on effect of leading to much more heterogeneous
results — every software author-and-publisher comes up with their own unique way
of doing things.

Fundamentally, a PDF file isn’t any more “real” than a Git repository — the only
difference is that there is a large existing sociotechnical infrastructure built
around citing the kinds of research outputs that can be captured in PDFs, and
not Git repos.


# Making Software In-And-Of-Itself Citeable

Linking your software to a separate entity that has passed through a “real”
publisher is basically an easy way to foist the work of citeability-making off
on someone else. (As easy as it is to get a peer-reviewed article published,
that is.) The dissatisfying thing about this approach is that you have to ask
people to cite something that is *entirely distinct* from your actual software.
Imagine if things were the other way around — in order for you to get credit for
your new research article, you needed to get people to, say, install a certain
package from [PyPI], because your tenure case depended on hitting 100,000
downloads per month. No thank you!

[PyPI]: https://pypi.org/

Fortunately, there are now systems in place that assist you, the software
author-and-publisher, in making it so that your software can be cited directly.
We’ll highlight two.

## Zenodo

The free CERN-supported service [Zenodo] can take care of the nuts and bolts of
making software citeable: it accepts uploads of arbitrary files (e.g., source
code packages), guarantees their long-term preservation, and can mint associated
DOIs with proper metadata. Citations of those DOIs are, in as true a way as we
have, citations of the software itself.

[Zenodo]: https://about.zenodo.org/

In order to support multiple releases of the same piece of software, Zenodo
supports a concept called [DOI versioning][doiv]. To really do a gold-standard
job of publishing citeable software, you ought to understand how this versioning
works and set up some kind of automation to deposit every release of your
software with Zenodo. [GitHub has built-in support for this][ghdv] that probably
meets your needs. If you’re not using GitHub or want finer-grained control over
things, look into release automation tools such as [Cranko][crankodv].

[doiv]: https://zenodo.org/help/versioning
[ghdv]: https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content
[crankodv]: https://pkgw.github.io/cranko/book/latest/integrations/zenodo.html

## The Journal of Open Source Software

The free, open-access [Journal of Open Source Software][joss] (JOSS) takes a
slightly different tack to help make software citeable. JOSS is a “software
journal”: it looks and works like any other academic journal, but instead of
submitting manuscripts to it, you submit software. Your software is
peer-reviewed and, if it passes review, your software gets published. The JOSS
team takes on the work of minting a DOI and doing the other tasks to turn your
software into a citeable object.

[joss]: https://joss.theoj.org/about

People can get a bit confused by JOSS because during its submission process you
*do* have to submit a brief manuscript describing the software, and various JOSS
pages talk about “papers” published in the journal. But at its core, JOSS is
about peer-reviewing and publishing *software*, not prose. The associated
manuscript PDF is basically an adapter to help JOSS interface with legacy
scholarly-publishing workflows (and people) that have trouble understanding that
it’s possible to cite things that aren’t articles.


# Citation Instructions for Software In-And-Of-Itself

From the standpoint of fundamentals, having your software be citeable itself is
clearly superior to asking people to cite a proxy object such as a journal
article. As we just mentioned, though, a lot of people and tools still have
trouble figuring out how to cite things that aren’t journal articles. So if you
want the users of your software to cite it directly, you unfortunately have to
put a lot more effort into your instructions. Ideally you’d tell your users
exactly what steps they need to follow, but those steps depend on the policies
of the journals they’re submitting to — which, of course, you can’t know or
control!

[This AstroBetter blog post][absc] is aimed at authors of articles that cite
scientific software, showing examples of how such citations should look. While
it’s tuned for the astronomy community and its journals, much of its contents
are not field-specific. You might borrow from an appropriate section for your
own citation instructions.

[absc]: https://www.astrobetter.com/blog/2019/07/01/citing-astronomy-software-inline-text-examples/

If your software is relatively field-specific, you should probably base your
instructions on whatever guidelines are put forth by the major journals in your
field. Most journals will have, buried somewhere on their websites,
recommendations to authors about how to cite software generically; you can adapt
these to refer to your software specifically.


# Additional Resources

- [Katz et al. 2020: Recognizing the value of software: a software citation guide](https://doi.org/10.12688/f1000research.26932.2)
- [The FORCE11 Software Citation Principles](https://doi.org/10.7717/peerj-cs.86)
- [MIT Libraries: Citing & publishing software](https://libguides.mit.edu/software/citing)
- [Software Sustainability Institute: How to cite and describe software](https://www.software.ac.uk/publication/how-cite-and-describe-software)
- [The Software Citation Station](https://www.tomwagg.com/software-citation-station/)
