+++
title = "Writing Reference Material"
description = """\
  How to prepare reference material for your scientific software’s \
  documentation. \
  This guide is part of One Good Tutorial, a resource for people who are \
  documenting scientific software.\
"""

[extra]
section = "In-Depth Guides"
+++

**Reference material** is the portion of your documentation that provides a
concise, factual specification of the behavior of various aspects of your
software and how they are structured.

In many cases, most or all of your software’s reference material will consist of
**API documentation**. But it might also make sense for your reference material
to include specifications of on-disk file formats, relevant scientific concepts,
algorithms, data structure schemas, user interfaces, or domain-specific
languages, to name a few possibilities.


# The Purpose of Reference Material

The [Diátaxis framework][dtx] provides a schema for thinking about how the
reference material in your documentation interrelates with other elements, most
notably your [tutorial](@/in-depth/tutorial-planning.md) and any
[how-tos](@/in-depth/other-elements.md#how-to-guides) or
[explainers](@/in-depth/other-elements.md#explainers). Diátaxis frames reference
material as content intended for people who are working with your software in
the moment and need to get the answer to a specific technical question as
quickly as possible: “What are the allowed values that I can give to the
`method` parameter of the `solve()` function?” The most important insight
embedded in the Diátaxis framework is that reference material is just *one*
component of your documentation — and it almost surely not where new users
should find themselves. This insight can get obscured, however, because our
software documentation is predominantly authored using [tools that were created
    specifically to support reference-style API
    documentation](@/in-depth/authoring-tools.md#next-option-language-specific-tool).

[dtx]: https://diataxis.fr/

Another way to think of reference material is as non-narrative *substrate* or
*foundation* that supports the narrative components of your documentation
(tutorials, etc.). It is the source of definitions and specifications that can —
and should — be cross-linked from everywhere else. Ideally, whenever a narrative
piece of documentation mentions a specific aspect of your software, you should
know exactly what hyperlink to add to take readers to the part of your reference
material that defines or specifies that aspect.

Your foundation should be solid, of course: reference material should be
complete and correct. It should also be neutral and concise: this portion of
your documentation should only be “fun” to read in the sense that it’s fun to
solve problems efficiently. As it’s phrased [in Diátaxis][dtxref]: “One hardly
*reads* reference material; one *consults* it.”

[dtxref]: https://diataxis.fr/reference/


# Scope

From the discussion above, our aspiration is to write up a complete and correct
specification of our software; but this quickly runs into the barrier that this
is virtually impossible. Comprehensively specifying the behavior of even a
small, seemingly innocuous piece of code can be fiendishly difficult work. For
instance, a function might take a latitude and longitude as arguments.
Straightforward … or is it? In a loosely-typed language like Python, are the
argument values floating-point numbers? [Sexagesimal] strings? Either? Can they
be arrays? If floats, what are the units? What precision? How is a longitude of
400° handled? How about a latitude of +95°? How about an array where only some
values are invalid? Are the measurements [geographic or geodetic][geo]? What
[reference ellipsoid][refell] should be used? It can take a whole paragraph just
to really precisely specify the semantics of a single argument to a single
function ­— and there might be a textbook’s worth of contextual knowledge needed
to understand the specification (such as the difference between geographic and
geodetic coordinates).

[Sexagesimal]: https://en.wikipedia.org/wiki/Sexagesimal#Modern_usage
[geo]: https://en.wikipedia.org/wiki/Latitude#Geodetic_and_geocentric_latitudes
[refell]: https://en.wikipedia.org/wiki/Figure_of_the_Earth

Therefore it is essential to set a manageable scope for your reference material.
This is a place where your [personas](@/in-depth/personas.md) may be helpful. To
first order, your reference material should prioritize breadth over depth, but
your personas can offer guidance as to what topics should receive in-depth
treatment.


# Structure

While the prose of reference material should be efficient, so should its
structure. That is, as soon as a reader has a question, it should be as quick as
possible for them to pull up the sentence in the reference documentation that
answers it.

Therefore, much more so than narrative documentation, reference material would
ideally surface itself — always being “at the fingertips” of someone working
with your software. In the current technology ecosystem, this implies
integration with [IntelliSense]-type editor features, full-text search,
chatbots, and so on. In the not-so-distant future we will likely understand such
mechanisms as the *primary* ones by which readers access your reference
material. But in the nearer term, our existing tooling is very much oriented
around creating a hierarchical tree of reference documentation pages, and that
is the paradigm that One Good Tutorial targets.

[IntelliSense]: https://code.visualstudio.com/docs/editing/intellisense

Within such a paradigm, the goal of efficient access implies that the structure
of the reference material should be easy to navigate and, to the greatest extent
possible, reflect the conceptual structures of the thing being documented: it
forms a map.

The top level of your documentation hierarchy should have a “Reference” section
inside of which all reference materials are contained. The structure of the
materials within that section might take on a few forms.

## Example: Single Tree API Reference

For some software projects, you might start with only one “kind” of reference
material: API documentation for a single software module. Perhaps you’ll find
yourself adding substructure in the future, but start with the simplest
structure you can get away with.

The [reference documentation for the Bokeh visualization package][bokref]
follows this structure. The only reference material concerns the `bokeh` Python
package, and so the structure of the documentation follows the structure of the
package:

[bokref]: https://docs.bokeh.org/en/latest/docs/reference.html

> - Reference
>   - `bokeh`
>   - `bokeh.application`
>     - `bokeh.application.application`
>   - `bokeh.client`
>     - `bokeh.client.connection`
>     - `bokeh.client.session`
>       - `bokeh.client.session.ogt_example`
>   - [...]

If your API has some kind of deeply nested outer structure, you may wish to take
inspiration from the Python design maxim [“flat is better than nested”][pep20]
and flatten that structure in your documentation. The result often feels easier
to navigate:

[pep20]: https://peps.python.org/pep-0020/

> - Reference
>   - `bokeh`
>   - `bokeh.application`
>   - `bokeh.application.application`
>   - `bokeh.client`
>   - `bokeh.client.connection`
>   - `bokeh.client.session`
>   - `bokeh.client.session.ogt_example`
>   - [...]

## Example: Categorized Reference Section

Some projects might call for reference documentation that goes beyond a single
API. You might have APIs in multiple languages, file formats, concepts, and
more. In these cases, it is useful to set up the structure of your reference
section to group similar kinds of things being documented:

> - Reference
>   - Algorithms
>   - Concepts
>   - File Formats
>   - Python APIs
>   - Rust APIs

The [reference documentation for the Gatsby web framework][gatsref] is built
according to Diátaxis principles and partially adopts this structure. While some
of the top-level sections of the Gatsby reference section group by object type
(“Config Files”, “Release Notes”), others are topical (“Routing”, “Local
Development”):

[gatsref]: https://www.gatsbyjs.com/docs/reference/

> - Reference
>   - Overview
>   - Cloud
>   - Local Development
>   - Built-In React Components
>   - Routing
>   - Config Files
>   - Functions
>   - GraphQL Data Layer
>   - Rendering Options
>   - Release Notes

Qualitatively, it can often be easier to navigate a categorical (kind-based)
structure because individual items being documented can easily be relevant to
multiple topics.


# Content

The golden rule of writing reference material is: *include examples everywhere*.
Prose descriptions of technical objects are often necessary in reference
material, but in your own experience you’ve probably noticed how helpful it is
to see the thing itself rather than read about it — even if “the thing” is
something intangible like a data structure.

This may seem inconsistent because examples sound suspiciously like “tutorial”
or “how-to” material, which Diátaxis argues should be kept separate from
reference material. The answer is that examples belong *everywhere* in your
documentation, but that ones in your reference section should be in the
recommended reference style: terse and direct. However, it’s more than
appropriate for a reference definition to link to tutorials or other
documentation materials that demonstrate the use of the item in a narrative
context.

## Example: Example

Consider this description on its own:

> The returned value is a JSON object with a mandatory field `hits` consisting
> of a list of lists of integer Cartesian coordinates. If `hits` is empty, the
> object will also include a field `message` containing a human-readable message
> in English explaining why the query returned no hits.

Now add some examples to it:

> ### Example Results
>
> If the query matches two objects:
>
> ```json
> {"hits": [[0, 3], [-4, 5]]}
> ```
>
> If the query returns no matches:
>
> ```json
> {"hits": [], "message": "Query did not overlap the target field"}
> ```

Most people read examples first and only “fall back” to reading the prose
description under duress. Your examples should therefore demonstrate important
pitfalls or corner cases — some readers simply won’t read your prose at all.

## Doctesting

It is of the utmost importance that your examples are actually correct! Most
language-specific documentation tools include **doctesting** frameworks that aim
to help ensure this by running the example code in your documentation.

It can be a bit of a hassle to set up doctesting because API examples often need
a lot of hidden boilerplate in order to become runnable. *It is worth the
effort.* Without doctesting, there are so many ways for your examples to get
out-of-date with regards to your implementation code, and few things break user
trust more than a non-working example. It’s also true that a doctesting regime,
paired with a nice supply of examples, will help you catch mistakes like
unintended API breakages during development — they are a valid and important
component of your overall testing regimen.

It therefore goes without saying that you should integrate your doctesting tool
into your continuous integration (CI) workflows — another benefit of the
[docs-as-code][dac] approach.

[dac]: https://www.writethedocs.org/guide/docs-as-code/

### Selected Doctesting Resources

- [Sphinx: Test snippets in the documentation](https://www.sphinx-doc.org/en/master/usage/extensions/doctest.html)
- [GitHub: koaning/mktestdocs](https://github.com/koaning/mktestdocs) — doctests for MkDocs
- [The rustdoc book: Documentation tests](https://doc.rust-lang.org/rustdoc/write-documentation/documentation-tests.html)


# Additional Resources

- [Diátaxis: Reference](https://diataxis.fr/reference/)
- [Diátaxis: The difference between reference and explanation](https://diataxis.fr/reference-explanation/)
- [Write the Docs: How to write API documentation](https://www.writethedocs.org/guide/#how-to-write-api-documentation)
- [The Good Docs Project: Reference template guide](https://www.thegooddocsproject.dev/template/reference)
- [The Good Docs Project: API Reference template guide](https://www.thegooddocsproject.dev/template/api-reference) (for web APIs)
- [The Good Docs Project: Concept template guide](https://www.thegooddocsproject.dev/template/concept)
