# How documents are written in this repo

Every document declares its format in the header: `**Format:** Standard` or `**Format:** Free-form`.

## Standard (the default)

For findings with a verdict: hypothesis tests, COT findings, 13F summaries, field notes. Top to bottom:

1. **Headline verdict.** One or two plain sentences. A reader with no trading background understands the conclusion from this alone.
2. **Why it matters.** Two to four sentences.
3. **The evidence.** Tables, numbers, tests. Each non-obvious term is explained once, at first use.
4. **How we got here.** Method: data, definitions, test design, what would change the call.
5. **Caveats.** Brief.

One file, three layers: the short answer (1 and 2), the story (3 read as a narrative), and the full research (definitions, data, results, limitations, version and changelog, how to cite).

## Free-form

For reads where the form is part of the message: interactive pages, charts you can hover, tabs, filters, scroll stories. A free-form document may choose its own layout, look and interactions, and may be a hosted page with a markdown companion. Any finding can opt in, for example a COT explorer that reads better when you can filter it.

What free-form can change: layout, look, interactivity, format.

What free-form cannot drop:

1. **A plain-English headline verdict**, in the page or in its markdown companion.
2. **Every number traceable.** Hover or click shows the source. Each figure is marked as a primary filing, secondary coverage, our math, or our view.
3. **Data and sources committed in this repo**, so the page can be rebuilt and checked.
4. **A markdown companion** in the standard layers, so the read works without scripts and can be cited and archived.
5. **Version, date, changelog and how to cite.**
6. **No positions, account details or dollar exposure, and no recommendation to buy or sell.**
7. **No trackers and no login.**

## Statuses

Findings carry one status:

- **Confirmed:** passed every test declared in advance. Eligible to become a rule; only the author promotes it.
- **Rejected:** failed, or went the opposite way.
- **Shelved:** inconclusive, or no usable data. Not retested without a new hypothesis.
- **Running:** the definition is frozen and evidence is still being collected. It ends in one of the three above.

There is no "Mixed". Company and sector reads carry no verdict status; they carry a published date and a last-updated date.
