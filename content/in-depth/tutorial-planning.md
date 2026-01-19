+++
title = "Planning a Tutorial"

[extra]
section = "In-Depth Guides"
+++

**Tutorials** teach users what it’s like to use your software. They assume that
your user has some relevant background knowledge (aligned with your
[personas](@/in-depth/personas.md)) and a
[synopsis](@/in-depth/synopsis.md)-level idea of what your software does, but
nothing more. A tutorial sets up a problem and shows how your software can solve
it, holding the users’ hand the entire way.

Tutorials are especially important because they are the best way to turn
*potential* users into *actual* users of your software. People searching for
general information about your software should see the metaphorical equivalent
of bright flashing lights directing them to its [installation
instructions](@/in-depth/installation-instructions.md) and your best tutorial.
While other elements of your documentation and, dare we say it, marketing will
affect the uptake of your software, an excellent tutorial is one of your best
assets for driving [conversions].

[conversions]: https://en.wikipedia.org/wiki/Conversion_marketing


# The Purpose of Tutorials

The [Diátaxis framework][dtx] provides a schema for thinking about how tutorials
interrelate with other elements of your software’s documentation, most notably
the [reference material](@/in-depth/reference-material.md) and any
[how-tos](@/in-depth/other-elements.md#how-to-guides) or
[explainers](@/in-depth/other-elements.md#explainers). All of these other
materials are essentially aimed at people who are *already* users of your
software. In Diátaxis, reference materials and how-tos are for users who are
actively trying to use your software to solve a specific problem, while
explainers are aimed at people who are invested enough to want to understand the
“whys” of your software better.

[dtx]: https://diataxis.fr/

Tutorials are unique in their relevance to new users. They’re for people who are
interested in your software but *don’t yet know what kinds of problems it can
really solve*. Now, you might also write tutorials aimed at users who are
familiar with one part of your software, but novices when it comes to a separate
part; but One Good Tutorial emphasizes that you should have one (good) tutorial
that is consciously aimed at first-timers. It need not — and, depending on the
complexity of your project, perhaps *should* not — try to each them everything
about what your software does. Instead the goal is to teach the user why your
software exists.


# The Purpose of Tutorial Planning

Tutorials are lessons. While all documentation is education, that’s more true of
tutorials than of any other element that you’ll write. This may be a bit
intimidating: education is a rather prominent unsolved problem of human
civilization. Regardless of your specific beliefs about what constitutes truly
excellent teaching, you’ve probably encountered it only rarely in your life. We
can hand you no foolproof manual on how to craft an outstanding educational
experience.

But **if there’s one place in your software’s documentation to get ambitious,
this is it.** Whatever energy you have for going above-and-beyond in preparing
your documentation is best spent on your tutorial. And regardless of how good of
a teacher you think you are, there *is* one foolproof technique to doing the
best job of it you possibly can: plan ahead, then iterate, iterate, iterate.


# Outline First

The goal for the tutorial planning stage should be to generate an **outline** or
**storyboard** sketching out your intended tutorial experience. Either way, the
initial product is totally informal and not intended for public consumption.

There’s no rule that says that you can’t immediately plunge into drafting your
tutorial itself, of course. But the purpose of outlining first is to think
through the end-to-end tutorial experience *without* producing any actual
material that you would feel bad about throwing away. The recommendation of [the
One Good Tutorial playbook](@/playbook.md) is to prepare your outline early,
then switch to working on a few other lower-stakes elements of your
documentation. That way, you have some time for your tutorial plan to simmer in
the background. If you end up feeling like maybe you should revisit your parts
of it, trust that instinct — usually it’s onto something.


# Planning Your Pedagogy

The [Diátaxis discussion of tutorials][dtxtut] provides a very good set of
suggestions for how to design of your tutorial as an educational experience.
Read it and think about what kind of tutorial experience based on your software
will hit your preferred pedagogical touchstones, such as:

[dtxtut]: https://diataxis.fr/tutorials/

- Delivering visible results early and often
- Targeting a feeling of doing
- Maximally reliable operation

Again, your tutorial need not demonstrate everything your software can do. It
also need not demonstrate the aspects of your software that you consider to be
most impressive or complex. But it should help people understand what makes your
software unique. If you’ve got a new tool to do a calculation that’s implemented
in a preexisting piece of software that’s incredibly popular in your field,
people had better come away with a crisp understanding why they might want to
use your code instead of the same thing they’ve already got installed and have
been using for a decade.

The Diátaxis guide actively *discourages* tutorials from spelling out their
learning goals explicitly (“Show the learner where they’ll be going”). The idea
is that it is better to focus on tangible results (“In this tutorial we will
calculate and plot the synchrotron spectrum of a typical astrophysical plasma”)
rather than hoped-for learning outcomes, which you cannot actually control (“You
will learn that the Dulk (1985) synchrotron approximations are not very accurate
and you should use my software to do a better job”). Your behind-the-scenes
documentation notes are a good place to record the hoped-for outcomes, though.


# Planning Your Implementation

You should start planning your tutorial educational experience focusing purely
on its pedagogical design. Early on in the design process, though, you should
start considering the tangible form that your tutorial will take.

## Form Factor

This is another opportunity to get ambitious and question assumptions. Most of
your software’s documentation will probably take the form of linear prose, but
that’s not your only option: is your tutorial best delivered as a video? A
[slide deck](@/playbook.md)? Something else? While your tutorial will almost
surely be delivered as web content, modern web browsers can deliver virtually
*any* kind of interactive, multimedia experience that you can dream up.

That being said, you probably don’t have the resources to get completely
pie-in-the-sky. Your realistic options are going to be limited by your time,
background knowledge, and your [authoring tools](@/in-depth/authoring-tools.md).
If there’s a particular effect you’d like to achieve, now is the time to do some
research and see if you can realistically make it happen. Many popular authoring
tools such as [Sphinx] have [extension libraries] that might contain an
implementation of exactly the feature you need.

[Sphinx]: https://www.sphinx-doc.org/
[extension libraries]: https://www.sphinx-doc.org/en/master/usage/extensions/index.html

You should also consider any prerequisites that people will need to satisfy
before they can even start your tutorial. The fewer of these, the better.
[Ideally](@/in-depth/installation-instructions.md), your software would be so
easy to install that it will present no barrier to anyone, but if that’s not the
case, it may be worth setting up a cloud-based option (e.g. [MyBinder]) so that
users can run your code without having to install your software locally.

If it’s really necessary, there’s no reason that you can’t publish a passive
“tutorial” that shows users through what *would* happen if they installed and
ran your code, but this should be a last resort, reserved for situations where
it’s simply not possible for someone to usefully install your software on their
own. (For instance, the software might be nonfunctional until you grant access
to a proprietary dataset.) In these cases, a recorded video demo might hold
people’s attention better than a long prose document.

[MyBinder]: https://mybinder.org/

## Affordances

While planning your tutorial, keep in mind that *you can alter the thing that is
being taught* ­— that is, your software. If some aspect of your software is hard
to explain, that’s an indication that you should consider a redesign! If there
is a sequence of steps that need to be repeated identically, you should probably
create a helper method that automates them! Instead of documenting why something
is confusing or inconvenient, it is far better to take the time to *actually fix
the problem.* As a bonus, any improvements that you make in support of your
tutorial will probably come in handy for *all* users of your software, not least
yourself.

This consideration applies to all aspects of your software’s design, not just
APIs. If your software needs data resources in order to run, consider setting up
infrastructure so that it can download them automatically — this takes work, but
can be transformative for ease-of-use. Likewise for automating or removing any
initial configuration, or at least making relevant operations [idempotent] and
resources [immutable]. Really, these are general principles of good software
design that are relevant far beyond your tutorial — but the planning of your
tutorial is a good spur to revisit them, and it’s helpful to be able to focus on
the areas relevant to your tutorial and try to avoid spiraling into feeling like
you need to rewrite your entire project.

[idempotent]: https://en.wikipedia.org/wiki/Idempotence#Computer_science_meaning
[immutable]: https://web.mit.edu/6.005/www/fa15/classes/09-immutability/



# Additional Resources

- [Diátaxis: Tutorials](https://diataxis.fr/tutorials/)
- [Diátaxis: The difference between a tutorial and a how-to guide](https://diataxis.fr/tutorials-how-to/)
- [The Good Docs Project: Tutorial template guide](https://www.thegooddocsproject.dev/template/tutorial)
