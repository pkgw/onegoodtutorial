+++
title = "The Checklist"
template = "checklist.html"
+++

<!-- A lot of action is in the HTML template, but here is where we define the info text -->

{% checklist_info(phase="p", item="synopsis") %}
Here's the info for synopsis-plan.
{% end %}

{% checklist_info(phase="p", item="personas") %}
Here's the info for personas-plan.
{% end %}