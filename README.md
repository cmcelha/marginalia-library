# Marginalia Library

Curated, hand-vetted splits of public-domain texts for the [Marginalia](https://github.com/cmcelha/marginalia) Cowork plugin.

Each text is split into hierarchical study units (short / medium / long tiers) with frontmatter groupings that the Marginalia daily-lesson skill reads to deliver passages at the user's chosen cadence.

## Currently available

*(library.json is the source of truth — this list will track it)*

- **The Art of War** — Sun Tzu, tr. Lionel Giles (1910) · 59 short units / 13 chapters
- **Tao Te Ching** — Lao Tzu, tr. James Legge (1891) · 81 short units / 81 chapters
- **Meditations** — Marcus Aurelius, tr. George Long (1862) · 89 short units / 12 books
- **The Analects of Confucius** — Confucius, tr. James Legge (1893) · 74 short units / 20 books
- **The Enchiridion** — Epictetus, tr. George Long (1877) · 52 short units / 52 chapters
- **The Prince** — Niccolò Machiavelli, tr. W. K. Marriott (1908) · 69 short units / 26 chapters
- **The Bhagavad Gita** — tr. Sir Edwin Arnold (1885) · 46 short units / 18 chapters
- **The Nicomachean Ethics** — Aristotle, tr. D. P. Chase (1847) · 159 short units / 10 books
- **Thus Spake Zarathustra** — Friedrich Nietzsche, tr. Thomas Common (1909) · 145 short units
- **The Quran** — tr. J. M. Rodwell (1861) · 268 short units / 114 surahs
- **The Torah (Five Books of Moses)** — JPS 1917 · 216 short units / 5 books
- **Principal Upanishads** — tr. Swami Paramananda (1919) · 33 short units (Isa, Katha, Kena)
- **The Bible (World English Bible)** — public domain (2000) · 1007 short units / 66 books
- **Confessions** — Augustine, tr. E. B. Pusey (1838) · 152 short units / 13 books
- **The Dhammapada** — tr. F. Max Müller (1881) · 26 short units / 26 chapters
- **The Great Learning & Doctrine of the Mean** — tr. James Legge (1861) · 28 short units
- **The Imitation of Christ** — Thomas à Kempis, tr. William Benham (1874) · 141 short units / 4 books
- **On Liberty** — John Stuart Mill (1859) · 76 short units
- **The Rubáiyát of Omar Khayyám** — tr. Edward FitzGerald (1889) · 15 short units
- **The Thirty-Six Stratagems** — Marginalia editors, from public-domain chengyu · 36 short units

## Structure

```
marginalia-library/
├── library.json              # index of available texts
├── README.md
├── CONTRIBUTING.md           # how to add a new split
├── art-of-war/
│   └── art-of-war.md         # bundled with the plugin too; here for reference
├── meditations/
│   └── meditations.md
├── ...
└── bible-web/
    ├── library.json          # sub-index (Bible per book)
    └── books/
        └── ...
```

Each text directory contains a single markdown file with YAML frontmatter (title, translator, year, license, source URL, unit counts, groupings) and the body split into chapter + unit headings with blockquoted passages.

## Public domain only

This library only accepts translations that are public domain in the United States. As a general rule: first published before 1930, or with an explicit PD license (like the World English Bible). See `CONTRIBUTING.md` for the verification checklist.

Notable refusals:
- Walter Kaufmann's Nietzsche translations (in copyright)
- Victor Harris's *Book of Five Rings* translation (in copyright; no PD English translation of Musashi exists)
- Penguin Classics translations post-1930
- Foucault, Chomsky, and other 20th-century theorists' works (in copyright)

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the format spec and PR checklist.
