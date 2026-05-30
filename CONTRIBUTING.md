# Contributing to the Marginalia library

Thanks for wanting to add a text. The library is opinionated about format and quality — please read this whole guide before opening a PR.

## What we accept

- **Public-domain translations** of texts worth slow reading
- **High-quality splits** that respect natural verse/section structure
- **Hierarchical units** with short, medium, and long groupings baked in

## What we don't accept

- Translations still in copyright (see the refusal list in the README)
- "Auto-split" texts that haven't been reviewed for unit-boundary quality
- Texts that aren't substantively re-readable (this is a slow-reading library, not a general ebook host)
- Modern paraphrases or "simplified" versions

## The format

Each text is a single markdown file with YAML frontmatter and a hierarchical body. See the [Marginalia plugin's `add-text` skill reference](https://github.com/cmcelha/marginalia/blob/main/skills/add-text/references/library-json-schema.md) for the full schema. Quick version:

```markdown
---
title: Meditations
author: Marcus Aurelius
translator: George Long
translation_year: 1862
license: public domain
source_url: https://www.gutenberg.org/files/2680/2680-0.txt
short_units: 130
medium_units: 24
long_units: 12
groupings:
  medium:
    - {units: [1, 2, 3, 4, 5], title: "Book I — Personal debts"}
    ...
  long: by-chapter
---

# Book I — Personal debts

## Unit 1 — Book I, sections 1-3: Honour from family

> 1. From my grandfather Verus I learned good morals and the government of my temper.
> ...
```

## How to produce a new split

The recommended path is to use the Marginalia plugin's `split-text` skill on a Project Gutenberg source URL. Then review the auto-split for boundary quality before submitting. The skill produces an 80%-of-the-way split that almost always needs minor editorial cleanup.

Manual splits are also welcome and often higher quality, especially for texts with idiosyncratic structure (Bible per book, Quran by surah, multi-volume Vedic texts).

## Unit-boundary guidance

- **Short units** = 200-500 words. Respect verse/section breaks; don't cut mid-argument.
- **Medium groupings** = 1500-3000 words. Default to chapter boundaries; sub-divide long chapters thematically.
- **Long groupings** = 3000-6000 words. Typically = chapter (use `long: by-chapter` shorthand).

See the `split-text` skill's main SKILL.md in the plugin repo for the full boundary heuristics.

## PR checklist

- [ ] Translation is public domain (verify translator + year; cite source)
- [ ] Frontmatter complete with all required fields
- [ ] `short_units` count in frontmatter matches actual `## Unit N` count in body
- [ ] Groupings table covers every short unit (no gaps, no overlaps)
- [ ] Unit titles are descriptive themes, not summaries (no spoilers)
- [ ] Verse numbers preserved from the source
- [ ] Gutenberg license boilerplate removed from body (attribution stays in frontmatter)
- [ ] Entry added to root `library.json`
- [ ] Spot-checked at least 3 random units for cleanliness

## Code of conduct

Be kind. Disagreements on split boundaries are normal — defer to the reviewer's experience with the specific text, but bring evidence (verse numbers, structural arguments) rather than vibes.
