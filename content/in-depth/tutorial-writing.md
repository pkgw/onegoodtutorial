+++
title = "Writing a Tutorial"
description = """\
  How to write a scientific software tutorial. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

Once you have [planned your tutorial][plan] and [selected your authoring
tools](@/in-depth/authoring-tools.md), there’s nothing left but to sit down and
write it. This guide provides suggestions and resources that aim to ease that
task, assuming that you already have an outline or storyboard in hand.

[plan]: @/in-depth/tutorial-planning.md


# Pedagogical Style

As emphasized in [the planning guide][plan], a tutorial is a lesson — it’s
teaching. It’s an especially challenging form of teaching, in fact, since in a
prewritten tutorial, there’s a wall between teacher and student: you can’t
observe and course-correct as your readers get confused by ambiguous terms, run
into unexpected errors, or skip past important points.

[The Diátaxis explanation of tutorials][diatut] provides a number of
recommendations for effective tutorial pedagogy. You need not buy into all of
them, but you are strongly encouraged to take to heart at least the following:

[diatut]: https://diataxis.fr/tutorials/

- *Ruthlessly minimize explanation.* The tutorial is *not* the time to go into
  reasons for things. Just tell the reader that something needs to be done, and
  they will trust that there’s a reason for it. Hyperlinks to more detailed
  documentation can satisfy the curiosity of the overachievers.
- *Ignore options and alternatives.* Stay focused and streamlined. Not only is
  this more helpful for the learner, it means less work for you!
- *Aspire to perfect reliability.* This point should speak for itself. Your
  tutorial is your best chance to build trust with a potential user. If you
  succeed, they’ll forgive you for all sorts of confusions or oddities farther
  down the line. If you fail, you’ve probably lost your chance to acquire a
  committed user. And no matter how visually polished and clever your tutorial
  is, your reader isn’t going to trust you if it doesn’t actually work.

In your documentation notes you might try writing down a Diátaxis-like set of
principles summarizing the pedagogical approach you wish to take in *your*
tutorial(s).

One Good Tutorial recommends that your tutorial *not* include “exercises”, or
really any elements that require the user to make a decision. They’re basically
all downside — no one’s going to refuse to use your software because your
tutorial was *too easy*, but you might lose someone who doesn’t understand a
prompt or gets stuck for just a few seconds too long on what you thought was a
trivial fill-in-the-blank. Ideally, someone should be able to successfully
complete your tutorial with their brain fully turned off, just copy/pasting
sample code or commands and reading basically *none* of the prose that separates
them. You might (or might not) be surprised at the number of highly-credentialed
PhD holders who will literally do this!


# Prose Style

Your tutorial is likely to be one of the least formal elements of your
software’s documentation, but it’s still a piece of **technical writing**. There
are professional technical writers whose entire careers are devoted to refining
the craft of delivering crystal-clear descriptions of complex topics — and
you’re probably not one of them. Fortunately, you can still profit from their
insights.

The [Write The Docs Software Documentation Guide][sdg] provides a wealth of
advice about technical writing style, as well as a number of related topics.

[sdg]: https://www.writethedocs.org/guide/

There are a number of other freely-available technical writing guides as well,
just a web search away. Your organization may already have an officially adopted
technical style guide.


# Visual Style

The overall visual appearance of your tutorial will be largely controlled by the
styling of your [authoring tool](@/in-depth/authoring-tools.md). Most such tools
offer some sort of themeing or templating functionality. Spend some time
exploring the options to find one that strikes you as clean and easy-to-read.
Browsing a “theme gallery” can really emphasize the range of possibilities even
within a fairly constrained design space.

Your tutorial will likely include numerous blocks of sample code and/or commands
to run. Ensure that these are rendered with appropriate **syntax highlighting**,
which makes a world of difference for readability. If at all possible, try to
ensure that direct copy/pasting of your code blocks will yield correct results.
Comment your code generously ­— strangely, people will read the comments in your
code blocks much more readily than they will read the prose that comes before or
after them:

```py
# see what I mean?
energy = np.dot(m, v**2)
```

Try also to hyperlink generously from your tutorial to more detailed
documentation, or take notes about what hyperlinks *should* be added if the
other elements of your documentation haven’t been written yet. It is possible to
get to the point where a certain block of text has too many links, but it takes
a while to get there.


# User Testing

The [reference material guide](@/in-depth/reference-material.md) mentions the
importance of **doctesting** — setting up tooling to check that any code
examples in your tutorial stay valid and runnable. You should also think
seriously about doing some **user testing** of your tutorial — that is, asking a
colleague or two to work through it while you watch. This can be a hassle to
arrange, and you might find the whole idea stressful, but *user testing is by
far the best way to ensure that your tutorial actually works well*.

As with technical writing, there are professionals who spend their entire
careers doing, and thinking about, sophisticated user testing. Once again, you
are probably not one of these people. Nor do you have the resources of a major
tech company at your disposal.

That’s OK. Even rudimentary, amateurish user testing is worthwhile and might
reveal important facts about your tutorial. Just point someone at your tutorial,
ask them to “do it” without further explanation, and watch what they do. Resist
the temptation to intervene with any mistakes until you’re convinced that you
won’t learn anything more by watching your test subject continue to flail
around.


# Additional Resources

- [Google: Technical writing resources](https://developers.google.com/tech-writing/resources)
- [GitLab University: Technical writing fundamentals course](https://university.gitlab.com/courses/gitlab-technical-writing-fundamentals) (registration required)
- [sphinx-themes.org: Sphinx Themes Gallery](https://sphinx-themes.org/)
- [Timothée Mazzucotelli: MkDocs theme gallery](https://pawamoy.github.io/mkdocs-gallery/)
- [jekyllthemes.io: GitHub Pages themes](https://jekyllthemes.io/github-pages-themes)
- [Nielsen Norman Group: Usability Testing 101](https://www.nngroup.com/articles/usability-testing-101/)
