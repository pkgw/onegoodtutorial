+++
title = "The Playbook"
template = "playbook.html"

[extra]
footerclass = "symmetric"
+++

<!-- HTML template provides the reveal.js scaffolding -->

<section>
  <h2 class="tctr"><i>Welcome!</i></h2>

  <p>This <b>playbook</b> walks you through a method for creating
  documentation for your software project. It hits all of the items on
  <a href="..">the One Good Tutorial Checklist</a>.</p>

  <p>The playbook is delivered as a slide deck. On larger screens, navigate using the buttons in the
  lower-right, the arrow keys on your keyboard, or swipe gestures.</p>

  <p>On smaller screens, scroll vertically in the usual way.</p>
</section>

<section data-background-color="rgb(227, 244, 254)">
  <h1>Part 0: Preliminaries</h1>

  <p class="tctr">A few points to address before we really get started.</p>
</section>

<section>
  <h2>Intended Audience</h2>

  <p>This playbook is aimed at authors of software projects that are:</p>

  <ul>
    <li>Small, DIY-style</li>
    <li>Open source</li>
    <li>Scientific</li>
  </ul>

  <p>We’d like to think that it will still have much to offer to participants
  in projects that do <i>not</i> meet these descriptions. But to keep
  focused we’ve avoided even mentioning some of the issues that arise in other
  circumstances.</p>
</section>

<section>
  <h2>Terminology</h2>

  <p>We assume that your documentation will be eventually published as HTML
  on the web, so we’ll refer to documentation <i>pages</i> and your overall documentation
  <i>site</i>. Reinterpret accordingly if you’re targeting a different medium.</p>

  <p>(Arguably, writing docs in the 21st century requires you to become a
  bit of a web developer. Fortunately, hosting services like <a href="https://readthedocs.org">ReadTheDocs.org</a>
  can take care of a lot of the hard parts for you.)</p>
</section>

<section>
  <h2>The Prime Directive</h2>

  <p>Above all else: this playbook is a <i>recommendation</i>, nothing more.
  Take inspiration from the parts that you like, ignore the ones that you don’t, and
  always trust your intuition. There’s no one
  “right” way to write docs, any more than there’s one right way to do anything
  else creative.</p>
</section>

<section data-background-color="rgb(227, 244, 254)">
  <h1>Part 1: Planning</h1>

  <p class="tctr"><i>“Plans are worthless, but planning is everything.”</i> —&nbsp;Dwight&nbsp;Eisenhower<sup><a href="https://en.wikiquote.org/wiki/Dwight_D._Eisenhower">*</a></sup></p>
</section>

<section>
  <h2>Step 1: Start A Notes Doc</h2>

  <p>It’ll be helpful to have some place to write down notes as you work on your
  docs — no need for these to be public. A Google Doc is fine. So is paper!</p>
</section>

<section>
  <h2>Step 2: Draft Your Synopsis</h2>

  <p>The <b>synopsis</b> is 1–3 sentences summarizing your software. Jot down
  a first draft in your notes.</p>

  <p><i>Example:</i> “<a href="https://pages.nist.gov/fipy/en/latest/">FiPy</a>
  is an object oriented, partial differential equation (PDE) solver, written in
  Python, based on a standard finite volume (FV) approach."

  <p><i>Why:</i> Your final synopsis will end up everywhere: at the top of your README
  or website, in announcements, maybe even grant proposals. Best to get a rough
  draft ASAP.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/synopsis/">Writing a Project Synopsis</a>.</p>
</section>

<section>
  <h2>Step 3: Think Up Some Personas</h2>

  <p>A <b>persona</b> is an imaginary, but specific, person who might use
  your software and documenation. Spend just a few minutes making up 2–3 named
  personas, and jot down brief profiles in a new section of your notes.</p>

  <p><i>Example:</i> “Postdoc Pete saw me give a talk about my software that
  computes model exoplanet spectra. He has observational data and is curious
  to see if my model matches, but won’t bother if it’s too hard to run.”

  <p><i>Why:</i> The design of your documentation (and your whole project) will be stronger
  if it targets specific kinds of people, not just a vague, generic “user”.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/personas/">Personas</a>.</p>
</section>

<section>
  <h2>Step 4: Outline Your Tutorial</h2>

  <p>Plan out a <b>tutorial experience</b> that will show new users how to accomplish
  something cool using your software. Record notes as an outline or storyboard.</p>

  <p><i>Why:</i> Your tutorial is your software’s make-or-break moment, so it should
  be as good as it can be. Planning it early helps you foresee any weak points.</p>

  <p><i>Example</i>: “Hmm, Undergrad Ursula is going to need to download a three-gigabyte
  data file for my tutorial. I need to figure out where
  to host it and tell her to kick off the download to run while she’s installing the code.”</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/tutorial-planning/">Planning a Tutorial</a>.</p>
</section>

<section data-background-color="rgb(227, 244, 254)">
  <h1>Part 2: “Easy” Drafts</h1>

  <p class="tctr">Next, we’ll focus on drafting some of the “easy stuff“. These are bits
  of documentation that your software really ought to have, but tend to be short and self-contained.
  When things go well, some of these might take only a few minutes to write.</p>
</section>

<section>
  <h2>Step 5: Draft Install Instructions</h2>

  <p>Draft your <b>installation instructions</b> in a new section of your notes document.</p>

  <p><i>Example:</i> “<a href="https://www.plasmapy.org/">PlasmaPy</a> may be installed from the
  command line using pip: <code>pip install plasmapy</code>”

  <p><i>Why:</i> Your instructions should be <i>extremely short</i> — the modern
  computing world has tons of tools that make it easy to install all kinds of software.
  Complicated install instructions are a sign that you’ve got engineering work to do.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/installation-instructions/">Installation Instructions</a>.</p>
</section>

<section>
  <h2>Step 6: Draft Citation Instructions</h2>

  <p>Draft your <b>citation instructions</b> in a new section of your notes document.</p>

  <p><i>Example:</i> “<a href="https://doi.org/10.1002/jcc.23981">Libcint: An efficient general
  integral library for Gaussian basis functions</a>, Q. Sun, J. Comp. Chem. 36, 1664 (2015)”

  <p><i>Why:</i> Unfortunately, many users of scientific software need to be reminded to cite it
  appropriately. Software citation practices also vary widely between fields, so even those who
  know to cite your software will need to be told how to do so. Everybody wins if you provide
  easy, prominent, and firm guidance.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/software-citation/">Software Citation</a>.</p>
</section>

<section>
  <h2>Step 7: Draft Licensing Statement</h2>

  <p>Draft a <b>licensing statement</b> in a new section of your notes document.</p>

  <p><i>Example:</i> “This project is licensed under the <a href="https://opensource.org/license/mit">MIT License</a>.”

  <p><i>Why:</i> Formally, people aren’t even allowed to download your software if you don’t provide
  certain basic information about its legal status. Don’t panic, though — in most cases, you
  just need to provide a few boilerplate sentences. But you should understand what they mean.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/licensing-statements/">Licensing Statements</a>.</p>
</section>

<section>
  <h2>Step 8: Draft Acknowledgments</h2>

  <p>Draft <b>acknowledgments</b> in a new section of your notes.</p>

  <p>You’re encouraged, but not obligated, to mention One Good Tutorial in your acknowledgments.</p>

  <p><i>Example:</i> “The MolSSI is supported by the U.S. National Science Foundation through grant number CHE-2136142.”

  <p><i>Why:</i> If a funder supported work on a software project, they almost surely should
  be acknowledged somewhere in your documentation. Take a few minutes to make sure that all
  funding sources are listed properly.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/acknowledgments/">Acknowledgments</a>.</p>
</section>

<section>
  <h2>Step 9: Draft Contribution Statement</h2>

  <p>Draft a <b>contribution statement</b> in a new section of your notes document.</p>

  <p><i>Example:</i> “The <a href="https://www.astropy.org/contribute.html">Astropy</a> project is made both by and for its users, so we accept contributions of many kinds …”

  <p><i>Why:</i> You should help other people understand if and how they can contribute to your
  software. New projects may not need more than an encouraging sentence or two. Popular
  projects might offer a more substantial Contribution Guide.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/contribution-statements/">Contribution Statements</a>.</p>
</section>

<section data-background-color="rgb(227, 244, 254)">
  <h1>Part 3: First Build</h1>

  <p class="tctr">It’s time to start turning your documentation from plans
  into reality — which means committing to some specifics.</p>
</section>

<section>
  <h2>Step 10: Scope Out Remaining Material</h2>

  <p>Make a list of other pages required for your “minimum viable”
  documentation. <a href="..">The checklist</a> calls for only one more element:
  <b>reference material</b>, such as API docs.</p>

  <p><i>Why:</i> One size does not fit all — now is the time to nail down
  what “good enough documentation” means to your project.</p>

  <p><i>Example:</i> “Beyond API docs, Developer Danielle is going to want to
  understand the schema of the JSON file that my tool emits.”</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/other-elements/">Other Common Documentation Elements</a>.</p>
</section>

<section>
  <h2>Step 11: Figure Out Authoring Tools</h2>

  <p>Select the tool(s) you’ll use to <b>author</b> your project’s documentation; integrate
  them into your project’s codebase. This may be quick if you’ve done this before, time-consuming if not.</p>

  <p><i>Example:</i> your entire documentation might fit comfortably in a single <code>README.md</code> file.</p>

  <p><i>Example:</i> <a href="https://www.sphinx-doc.org/">Sphinx</a>.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/authoring-tools/">Authoring Tools</a>.</p>
</section>

<section>
  <h2>Step 12: Stub Your Documents</h2>

  <p>Copy your “easy” draft texts into their intended places in your repository, and make
  minimal <b>placeholders</b> for the remaining documents that you’ve planned (“Tutorial goes here”).</p>

  <p>Look over the skeleton of your site.</p>

  <p><i>Why:</i> Now is a good time to experiment with the organization and style of
  your site. Is anything essential missing?</p>
</section>

<section>
  <h2>Step 13: Figure Out Publishing Tools</h2>

  <p>Select the tool(s) you’ll use to <b>publish</b> your project’s documentation; integrate them into
  your project’s codebase. Once again, this may be a time-consuming step if you haven’t set up
  this kind of workflow before.</p>

  <p>Validate the workflow by publishing your skeleton docs.</p>

  <p><i>Example:</i> <a href="https://docs.readthedocs.com/platform/stable/continuous-deployment.html">Continuous deployment</a>
  to <a href="https://readthedocs.org">readthedocs.org</a>.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/publishing-tools/">Publishing Tools</a>.</p>
</section>

<section data-background-color="rgb(227, 244, 254)">
  <h1>Part 4: Full Steam Ahead</h1>

  <p class="tctr">The foundations are in place, but you still need to
  draft some of your most important docs. Let’s tackle them.</p>
</section>

<section>
  <h2>Step 14: Draft The Tutorial</h2>

  <p>Write a first draft of your <b>tutorial</b>.</p>

  <p><i>Why:</i> Drafting the “easy” docs first has gotten you used to
  your tools and site layout. It’s time to take on a more open-ended
  writing project.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/tutorial-writing/">Writing a Tutorial</a>.</p>
</section>

<section>
  <h2>Step 15: Draft The Rest</h2>

  <p>Write up your <b>API reference</b> materials and any other documents
  that are still placeholders.</p>

  <p><i>Why:</i> Hopefully, the experience of writing the tutorial has
  helped you get a better understanding of which support materials are
  the most important, and what your examples should look like.</p>

  <p><i>In-Depth Guide:</i> <a href="/in-depth/reference-material/">Writing Reference Material</a>.</p>
</section>

<section>
  <h2>Step 16: Review and Revise</h2>

  <p>Take some time to <b>review</b> what you’ve written and <b>revise</b>
  anything that’s unclear or inaccurate. Hard-to-read docs often indicate
  an underlying engineering problem to address.</p>

  <p><i>Why:</i> “When you write a book, you spend day after day scanning
  and identifying the trees. When you’re done, you have to step back and
  look at the forest.” ―&nbsp;Stephen&nbsp;King<sup><a href="https://www.goodreads.com/quotes/370731-when-you-write-a-book-you-spend-day-after-day">*</a></sup></p>
</section>

<section>
  <h2>Step 17: Publish and Celebrate</h2>

  <p>That’s it! You’ve successfully written a set of documentation that will do
  credit to you and your project. Publish it and find a way to <b>reward
  yourself</b> for a job well done.</p>

  <p><i>Why:</i> Working on docs can feel like a slog — they’re never
  “finished,” and you’re probably all too aware of the shortcomings of
  whatever you’ve just written. This playbook has been designed to lead up
  to this tangible moment of victory, so go ahead and enjoy it!</p>
</section>

<section>
  <h2>Step 18 (Optional): Feedback</h2>

  <p>One Good Tutorial was developed by <a href="https://newton.cx/~peter/">Peter K. G. Williams</a>
  with the support of a <a
    href="https://bssw.io/pages/bssw-fellowship-program">Better
  Scientific Software (BSSw) Fellowship</a>.</p>

  <p>The BSSw organization
  would like to collect feedback about the user impact of this
  resource, so please consider <a href="https://www.surveymonkey.com/r/FDDF2ZW">taking this three-minute survey</a>
  about your experience.</p>

  <p>You can also reach out by creating an issue or pull request
  on the <a href="https://github.com/pkgw/onegoodtutorial/">One Good Tutorial GitHub repository</a>,
  or by <a href="https://newton.cx/~peter/about-me/#contact">contacting the author</a> directly.</p>
</section>