+++
title = "The Checklist"
template = "checklist.html"
+++

<!-- A lot of action is in the HTML template, but here is where we define the info text -->

{% checklist_info(phase="p", item="synopsis") %}
**This Step:** *Planning / Synopsis*

**Summary:** Jot down 1–3 *draft* sentences summarizing your software.

**Why:** Your final synopsis will end up everywhere: at the top of your README
or website, in announcements, maybe even grant proposals. Best to get a rough
draft ASAP!

{% end %}

{% checklist_info(phase="p", item="personas") %}
**This Step:** *Planning / Personas*

**Summary:** Imagine 1–3 “personas” of people who might be reading your
documentation.

**Why:** As you’re thinking about the different documents you’ll need to write,
it can be helpful to keep these user archetypes in mind. “Hmm, Postdoc Pete is
in too much of a hurry to follow this 20-step recipe!”

{% end %}

{% checklist_info(phase="p", item="tutorial") %}
**This Step:** *Planning / Tutorial*

**Summary:** Plan out a tutorial that will show new users how to accomplish
something cool using your software.

**Why:** *People learn by doing.* If someone has read your synopsis and is still
interested in your software, they’re not going to want to read pages of
additional text about it — they’re going to want to run your code ASAP and learn
what it “feels like”. The goal of your *one good tutorial* is deliver this
experience as painlessly as possible. Your tutorial is your software’s
make-or-break moment — so invest in it accordingly!

{% end %}

{% checklist_info(phase="p", item="installation") %}
TKTK: `plan-installation`.
{% end %}

{% checklist_info(phase="p", item="citation") %}
TKTK: `plan-citation`.
{% end %}

{% checklist_info(phase="p", item="license") %}
TKTK: `plan-license`.
{% end %}

{% checklist_info(phase="p", item="contributing") %}
TKTK: `plan-contributing`.
{% end %}

{% checklist_info(phase="p", item="api-ref") %}
TKTK: `plan-api-ref`.
{% end %}

{% checklist_info(phase="p", item="other-ref") %}
TKTK: `plan-other-ref`.
{% end %}

{% checklist_info(phase="p", item="acknowledgments") %}
TKTK: `plan-acknowledgments`.
{% end %}

{% checklist_info(phase="p", item="authoring-tools") %}
TKTK: `plan-authoring-tools`.
{% end %}

{% checklist_info(phase="p", item="release-process") %}
TKTK: `plan-release-process`.
{% end %}

<!-- Draft phase -->

{% checklist_info(phase="d", item="synopsis") %}
TKTK: `plan-synopsis`.
{% end %}

{% checklist_info(phase="d", item="personas") %}
TKTK: `plan-personas`.
{% end %}

{% checklist_info(phase="d", item="tutorial") %}
TKTK: `draft-tutorial`.
{% end %}

{% checklist_info(phase="d", item="installation") %}
TKTK: `draft-installation`.
{% end %}

{% checklist_info(phase="d", item="citation") %}
TKTK: `draft-citation`.
{% end %}

{% checklist_info(phase="d", item="license") %}
TKTK: `draft-license`.
{% end %}

{% checklist_info(phase="d", item="contributing") %}
TKTK: `draft-contributing`.
{% end %}

{% checklist_info(phase="d", item="api-ref") %}
TKTK: `draft-api-ref`.
{% end %}

{% checklist_info(phase="d", item="other-ref") %}
TKTK: `draft-other-ref`.
{% end %}

{% checklist_info(phase="d", item="acknowledgments") %}
TKTK: `draft-acknowledgments`.
{% end %}

{% checklist_info(phase="d", item="authoring-tools") %}
TKTK: `draft-authoring-tools`.
{% end %}

{% checklist_info(phase="d", item="release-process") %}
TKTK: `draft-release-process`.
{% end %}

<!-- Assess phase -->

{% checklist_info(phase="a", item="synopsis") %}
TKTK: `assess-synopsis`.
{% end %}

{% checklist_info(phase="a", item="personas") %}
TKTK: `assess-personas`.
{% end %}

{% checklist_info(phase="a", item="tutorial") %}
TKTK: `assess-tutorial`.
{% end %}

{% checklist_info(phase="a", item="installation") %}
TKTK: `assess-installation`.
{% end %}

{% checklist_info(phase="a", item="citation") %}
TKTK: `assess-citation`.
{% end %}

{% checklist_info(phase="a", item="license") %}
TKTK: `assess-license`.
{% end %}

{% checklist_info(phase="a", item="contributing") %}
TKTK: `assess-contributing`.
{% end %}

{% checklist_info(phase="a", item="api-ref") %}
TKTK: `assess-api-ref`.
{% end %}

{% checklist_info(phase="a", item="other-ref") %}
TKTK: `assess-other-ref`.
{% end %}

{% checklist_info(phase="a", item="acknowledgments") %}
TKTK: `assess-acknowledgments`.
{% end %}

{% checklist_info(phase="a", item="authoring-tools") %}
TKTK: `assess-authoring-tools`.
{% end %}

{% checklist_info(phase="a", item="release-process") %}
TKTK: `assess-release-process`.
{% end %}

<!-- Revise phase -->

{% checklist_info(phase="r", item="synopsis") %}
TKTK: `revise-synopsis`.
{% end %}

{% checklist_info(phase="r", item="personas") %}
TKTK: `revise-personas`.
{% end %}

{% checklist_info(phase="r", item="tutorial") %}
TKTK: `revise-tutorial`.
{% end %}

{% checklist_info(phase="r", item="installation") %}
TKTK: `revise-installation`.
{% end %}

{% checklist_info(phase="r", item="citation") %}
TKTK: `revise-citation`.
{% end %}

{% checklist_info(phase="r", item="license") %}
TKTK: `revise-license`.
{% end %}

{% checklist_info(phase="r", item="contributing") %}
TKTK: `revise-contributing`.
{% end %}

{% checklist_info(phase="r", item="api-ref") %}
TKTK: `revise-api-ref`.
{% end %}

{% checklist_info(phase="r", item="other-ref") %}
TKTK: `revise-other-ref`.
{% end %}

{% checklist_info(phase="r", item="acknowledgments") %}
TKTK: `revise-acknowledgments`.
{% end %}

{% checklist_info(phase="r", item="authoring-tools") %}
TKTK: `revise-authoring-tools`.
{% end %}

{% checklist_info(phase="r", item="release-process") %}
TKTK: `revise-release-process`.
{% end %}
