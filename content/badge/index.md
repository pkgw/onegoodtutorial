+++
title = "Badging for Checklist Compliance"
description = """\
  How to add a badge to your project’s README showing that you’ve adopted \
  the One Good Tutorial software documentation checklist. \
  This page is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "README badge"
+++

If you want to proclaim that your project’s documentation satisfies version 1 of
[the One Good Tutorial checklist](@/_index.md), consider adding a badge that
looks like this to your README, or wherever else is appropriate:

[![One Good Tutorial docs checklist v1: adopted](./adopted-v1.svg)](@/about/badge.md)

The Markdown code to create this badge is:

```md
[![One Good Tutorial docs checklist v1: adopted](https://onegoodtutorial.org/badge/adopted-v1.svg)](https://onegoodtutorial.org/about/badge/?v=1)
```

The equivalent in reStructuredText is:

```rst
.. image:: https://onegoodtutorial.org/badge/adopted-v1.svg
   :alt: One Good Tutorial docs checklist v1: adopted
   :target: https://onegoodtutorial.org/about/badge/?v=1
```

And finally, plain HTML:

```html
<a href="https://onegoodtutorial.org/about/badge/?v=1">
  <img src="https://onegoodtutorial.org/badge/adopted-v1.svg"
    alt="One Good Tutorial docs checklist v1: adopted" />
</a>
```

The code above will result in a clickable badge that takes people to [this
page](@/about/badge.md), which gives a short explanation of the One Good
Tutorial checklist concept.

Another way to advertise your use of the checklist is to [mention One Good
Tutorial in your
acknowledgements](@/about/index.md#citing-or-acknowledging-one-good-tutorial).
If you found One Good Tutorial useful, you’re encouraged — but not obligated —
to do so.