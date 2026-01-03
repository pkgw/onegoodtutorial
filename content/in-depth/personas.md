+++
title = "Personas"

[extra]
section = "In-Depth Guides"
+++

A **persona** is an imaginary, but specific, person who might use your software
and read your documentation. The technique of using personas is widely adopted
in fields like user experience (UX) design and marketing.

Ideally, a suite of personas is based on quantitative research about one’s users
or customers. In the context of One Good Tutorial, we instead assume an ad-hoc,
intuitive approach. If you have the resources to do some kind of customer
research, so much the better, but even a purely vibes-based process should still
be useful.

There’s no specific connection between the persona technique and documentation.
If you think of your scientific software as a *product* in the commercial sense,
you may find your personas useful in many aspects of your work on it: not just
documentation but UI/UX design, API design, feature selection, marketing, sales,
and more.


# Process

For the purposes of One Good Tutorial, we suggest that you try to devise three
personas. Each should be given a name and a few-sentence profile that captures
why they might be interacting with your software. At the scope of One Good
Tutorial, that’s all you need.

Your personas should generally represent groups of people that might
realistically become regular users of your software and its documentation. But
there can be some value in considering an “anti-persona” of someone who will
interact with your software but is *not* expected to become a user.

A collection of personas traditionally aims to span a variety of axes such age,
gender, location, and so on. For scientific software, there are several
more-specific dimensions that your personas might try to cover: career stage;
different subject-matter areas relevant to your software; and level of
familiarity with computing (or other tools and techniques relevant to your
software).

In general, your personas will be purely private thought experiments. But you
should construct them with the idea in mind that they might become public one
way or another. So if you’re a grad student advised by Prof. Smith, maybe don’t
compose a persona that starts “Prof. Smith is an impatient moron who knows
nothing about computers …”.


# Examples

Let’s make up some personas that might be relevant to the [Slurm][slurm] HPC
workload manager, focusing on academic users who might have reasons to go to the
Slurm documentation.

[slurm]: https://slurm.schedmd.com/

> Undergrad Ursula is a junior at the University of Iowa studying chemistry.
> She’s doing a research project with a professor using pre-existing Python
> scripts to compute some molecular parameters. She needs to run these scripts
> in parallel on the university’s HPC cluster. She’s never used Slurm before.

> Grad Student Grant is doing his PhD in geophysics. He is developing a new
> piece of parallel Python software to analyze large sets of seismic data. He
> took several computer science classes in college. His adviser has HPC
> experience but both of them are new to Slurm.

> Postdoc Pete is an economist trying to secure a permanent position. He’s
> working on analyzing a massive database of prices for a research paper and
> tries to work the R language whenever possible. He has access to a Slurm-based
> HPC cluster and has become convinced that he needs parallel processing to
> complete his analysis quickly, but hates spending his time on “computer
> stuff.”

> Developer Daria is research software engineer at a national lab. She’s been
> tasked with speeding up a mechanical engineering simulation written in C++.
> She’s an experienced Slurm user but is eager to learn about new features in
> case they help her squeeze more performance out of her code.

> Professor Penny is a professor of biology on a university committee overseeing
> the purchase of a new HPC cluster. The university research computing group is
> debating between installing Slurm and Torque, and has asked the committee for
> input on the decision. Penny oversees several grants that have major
> computational components, but when it comes to writing code she’s happily been
> “out of the trenches” for decades at this point.


# Additional Resources:

- [Wikipedia: Persona (user experience)](https://en.wikipedia.org/wiki/Persona_(user_experience))
- [Nielsen Norman Group: Personas make users memorable](https://www.nngroup.com/articles/persona/)
- [GitLab Product Handbook: Personas](https://handbook.gitlab.com/handbook/product/personas/) (more
  than a dozen personas used by the GitLab product team)

