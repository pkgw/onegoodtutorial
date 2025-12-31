+++
title = "Licensing Statements"

[extra]
section = "In-Depth Guides"
+++

A **licensing statement** informs users about the legal status of your code.

It may seem annoying and tedious to have to write up this information, and we
can’t honestly claim that it isn’t. But it’s important: formally, people aren’t
even allowed to download your software if you don’t provide the right
information. The good news is that in most cases, you only need to include a few
boilerplate sentences in the end. But you should understand what those sentences
mean.

# A Brief Primer on Copyright Law

*Disclaimer: we are not lawyers, this is not legal advice, yadda yadda yadda.
Don’t make any important decisions without talking to an actual expert. Also,
the following discussion is based on US law.*

You need to provide a licensing statement with your software because any
nontrivial source code is presumed to be copyrighted intellectual property. The
default stance of US copyright law is that if you get your hands on a
copyrighted work, you’re not allowed to duplicate it. This applies not only to,
say, photocopying printed books, but also to the mere act of downloading or
copying a digital file. So, in principle, even if I can trivially find your
source code on GitHub, legally speaking I can’t assume that I'm allowed to do
anything with it besides look at it.

**Licensing** is how the owner of a copyrighted work grants other people
additional rights vis-à-vis that work. By attaching a license to your code, you
can allow people to, well, actually download it and use it at all. This is why
software licensing is such a big deal!

But who owns a copyrighted work, anyway? The person who created it, you might
think. And that’s often true. But if you created something as part of your job,
your employer probably gets ownership. *This point is highly relevant to
scientific software!* Virtually every university and lab will have policies,
and often an entire office, devoted to managing the intellectual property
created by its employees.

There’s no magical central database of copyright owners, so it’s also important
to provide a **copyright statement** with your software identifying its legal
owner. This is the classic “Copyright 2025 {Your Name}” language that you see
everywhere. If you don’t provide this information, the software is “orphaned”:
it’s virtually impossible for anyone in the future to be sure of who actually
owns it, which means that it’s impossible to verify or modify its licensing
terms should the need arise.

There’s one more wrinkle worth mentioning: a work “prepared by an officer or
employee of the United States Government as part of that person's official
duties” is not eligible for copyright, and is instead part of the **public
domain**. It’s not copyrighted intellectual property; it’s just data. People can
duplicate it to their heart’s delight without worrying about licenses or
anything else. The documentation of public-domain software should still include
a legal statement, though, to make its public-domain status explicit.
