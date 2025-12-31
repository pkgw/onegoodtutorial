+++
title = "The Playbook"
template = "playbook.html"
+++

<!-- HTML template provides the reveal.js scaffolding -->

<section>
  <h2 class="tctr"><i>Welcome!</i></h2>

  <p>This <b>playbook</b> walks you through a method for creating
  documentation for your software project. It hits all of the items on
  <a href="..">the One Good Tutorial Checklist</a>.</p>

  <p>The playbook is delivered as a slide deck. Navigate using the buttons in the
  lower-right, the arrow keys on your keyboard, or swipe gestures.</p>
</section>

<section>
  <h1>Part 0: Preliminaries</h1>
  
  <p class="tctr">A few points to address before we really get started.</p>
</section>

<section>
  <h2>Intended Audience (1)</h2>
  
  <p>This playbook is aimed at authors of small, DIY-style software projects. We’d like
  to think that it will still have something to offer to participants in larger,
  more formalized projects, but to keep things focused we’ve avoided even
  mentioning some of the challenges that arise in bigger efforts.</p>
</section>

<section>
  <h2>Intended Audience (2)</h2>
  
  <p>This playbook is also aimed at authors of <i>scientific</i> software projects.
  We talk about a few issues, like citation, that other kinds of projects may not
  be concerned with. But most steps will be relevant to virtually any kind of
  software.</p>
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

<section>
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

  <p><i>In-Depth Guide:</i> <a href="/in-depth/contribution-statements/">Contribution Statements</a>.</p>
</section>

<section>
  <h1>Part 3: Scaffolding</h1>
  
  <p class="tctr">It’s time to start turning your documentation from plans into reality — which means
  committing to some specifics.</p>
</section>

<section>
  <h2>Step 10: Scope Out Remaining Material</h2>

  <p>Make a list of other materials that are required for your “minimum viable product” documentation.
  Most new software probably only needs one more element: some <b>reference material</b>
  supporting more-experienced users, like API documentation. Use your personas and the <a href="https://diataxis.fr/">Diátaxis</a>
  model to guide your thinking.</p>

  <p><i>Example:</i> “Beyond a Python API reference, Developer Danielle is really going to want to 
  see a schema for the JSON file that my analysis tool emits.”</p>

  <p><i>Why:</i> You probably have a lot of other things to do besides write documentation.
  Set a scope now and focus on just getting
  <i>something</i> out into the world — if it’s a success, you can always write more later.</p>
</section>

<section>
  <h2>Step 11: Figure Out Authoring Tools</h2>

  <p>Select the tool(s) you’ll use to <b>author</b> your project’s documentation and integrate
  them into your project’s codebase. This may be quick if you’ve done this before, time-consuming if not.</p>

  <p><i>Example:</i> your entire documentation might fit comfortably in a single <code>README.md</code> file.</p>

  <p><i>Example:</i> <a href="https://www.sphinx-doc.org/">Sphinx</a>.</p>
</section>

<section>
  <h2>Step 12: Stub Out Your Documents</h2>

  <p>Copy your “easy” draft texts into their intended places in your repository, and make 
  minimal <b>placeholders</b> for the remaining documents that you’ve planned (“Tutorial goes here”).</p>

  <p>Look over the skeleton of your site.</p>

  <p><i>Why:</i> Now is a good time to experiment with the organization and style of
  your site. Is anything essential missing?</p>
</section>

<section>
  <h2>Step 13: Figure Out Publishing Tools</h2>

  <p>Select the tool(s) you’ll use to <b>publish</b> your project’s documentation and integrate them into
  your project’s codebase. Once again, this may be a time-consuming step if you haven’t set up
  this kind of workflow before.</p>

  <p>Validate the workflow by publishing your skeleton docs.</p>

  <p><i>Example:</i> <a href="https://docs.readthedocs.com/platform/stable/continuous-deployment.html">Continuous deployment</a>
  to <a href="https://readthedocs.org">readthedocs.org</a>.</p>
</section>

<section>
  <h1>Part 4: Time to Write</h1>
  
  <p class="tctr">The pieces are all in place!</p>
</section>

<section>
  <h2>Step 14: Draft The Tutorial</h2>

  <p>Write a first draft of your <b>tutorial</b>.</p>
</section>

<section>
  <h2>Step 15: Draft The Rest</h2>

  <p>Write up your <b>API reference</b> materials and any other documents
  that are still placeholders.</p>
</section>

<section>
  <h2>Step 16: Review and Revise</h2>

  <p>You knew this step was coming: take some time to <b>review</b> what you’ve written and
  <b>revise</b> anything that’s unclear or inaccurate.</p>

  <p><i>Why:</i> TKTK</p>
</section>

<section>
  <h2>Step 17: Publish!</h2>

  <p>TKTK.</p>
</section>
