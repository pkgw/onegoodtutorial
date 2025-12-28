+++
title = "The Playbook"
template = "playbook.html"
+++

<!-- HTML template provides the reveal.js scaffolding -->

<section>
  <h2>Welcome!</h2>

  <p>This <b>playbook</b> walks you through a <i>suggested</i> set of steps to build up 
  documentation for your software project, in a way that will fill out
  <a href="/checklist/">the One Good Tutorial Checklist</a>.</p>

  <p>The playbook is delivered as a slide deck. Navigate using the buttons in the
  lower-right, the arrow keys on your keyboard, or swipe gestures.</p>
</section>

<section>
  <h1>Part 1: Planning</h1>
  
  <p class="tctr">We’ll start with some planning activities. A bit of
  preparation now can save a lot of time down the road!</p>
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
</section>

<section>
  <h2>Step 3: Think Up Some Personas</h2>

  <p>A <b>persona</b> is an imaginary, but specific, person who might use
  your software and read your documenation. Spend just a few minutes making up 2–3 personas.
  Give them names, and jot down notes about them.</p>

  <p><i>Example:</i> “Postdoc Pete works in my field and saw me give a talk about
  my software that computes model exoplanet spectra. He has observational data and wants
  to see if my models can reproduce them.”

  <p><i>Why:</i> The design of your documentation (and your whole project) will be stronger
  if it targets specific kinds of people, not just a vague, generic “user”.</p>
</section>

<section>
  <h2>Step 4: Envision Your Tutorial</h2>

  <p>Plan out a <b>tutorial experience</b> that will show new users how to accomplish
  something cool using your software. We’re not writing any text yet —
  just outlining.</p>

  <p><i>Why:</i> Your tutorial is your software’s make-or-break moment, so it should
  be as good as it can be. Outlining first helps us foresee the weak points and think
  about how we can address them.</p>

  <p><i>Example</i>: “Hmm, Undergrad Ursula is going to need to download a three-gigabyte
  data file in order to follow my tutorial. I need to figure out where
  to host it and tell her to kick off the download first so it can
  run in the background while she installs the code.”</p>
</section>

<section>
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
  computing world has tons of tools that make it easy to install all kinds of software. If
  your instructions are complicated, you probably ought to pause your docs work and spend
  some time figuring out how to integrate your software with one or more of these tools. It takes
  effort but it is <i>incredibly</i> worthwhile.</p>
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
</section>

<section>
  <h2>Step 7: Draft Licensing Statement</h2>

  <p>Draft a <b>licensing statement</b> in a new section of your notes document.</p>

  <p><i>Example:</i> “This project is licensed under the <a href="https://opensource.org/license/mit">MIT License</a>.”

  <p><i>Why:</i> Formally, no one is allowed to download your software if you don’t provide
  certain basic information about its legal status. Don’t panic, though — in most cases, you
  just need to provide a few boilerplate sentences. But you should understand what they mean.</p>
</section>

<section>
  <h2>Step 8: Draft Acknowledgments</h2>

  <p>Draft <b>acknowledgments</b> in a new section of your notes document.</p>

  <p><i>Example:</i> “The MolSSI is supported by the U.S. National Science Foundation through grant number CHE-2136142.”

  <p><i>Why:</i> If a funder supported work on a software project, they almost surely should 
  be acknowledged somewhere in your documentation. Take a few minutes to make sure that all
  funding sources are listed properly.</p>
</section>

<section>
  <h2>Step 9: Draft Contribution Instructions</h2>

  <p>Draft <b>contribution instructions</b> in a new section of your notes document.</p>

  <p><i>Example:</i> “The <a href="https://www.astropy.org/contribute.html">Astropy</a> project is made both by and for its users, so we accept contributions of many kinds …”

  <p><i>Why:</i> You should help other people understand if and how they can contribute to your
  software. New projects may not need more than an encouraging sentence or two. Popular
  projects might offer a more substantial Contribution Guide.</p>
</section>

<section>
  <h1>Part 3: Tools</h1>
  
  <p class="tctr">Your documentation is starting to take shape. The next task is to choose
  the tools that you’ll use to turn your plans into reality.</p>
</section>

<section>
  <h2>Step 10: Set Up Authoring Workflow</h2>

  <p>Select the tools you’ll use to <b>author</b> your project’s documentation and integrate them into your project’s
  codebase. Depending on your needs, a single tool may suffice, or you might need a multi-faceted approach
  integrating different tools that support multiple types of documents.</p>

  <p>Validate the workflow by stubbing out your tutorial with a placeholder that literally
  just says, “Tutorial goes here”.</p>

  <p><i>Example:</i> <a href="https://www.sphinx-doc.org/">Sphinx</a>.</p>
</section>


<section>
  <h2>Step 11: Set Up Publishing Workflow</h2>

  <p>Select the tools you’ll use to <b>publish</b> your project’s documentation and integrate them into
  your project’s codebase.</p>

  <p>Validate the workflow by publishing your tutorial placeholder.</p>

  <p><i>Example:</i> <a href="https://docs.readthedocs.com/platform/stable/continuous-deployment.html">Continuous deployment</a>
  to <a href="https://readthedocs.org">readthedocs.org</a>.</p>
</section>


<section>
  <h2></h2>

  <p><i>Example:</i></p>
</section>
