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
- **Apology, Crito, Phaedo** — Plato, tr. Benjamin Jowett (1892) · 72 short units
- **Bushido — The Soul of Japan** — Inazo Nitobe (1900) · 77 short units
- **The Consolation of Philosophy** — Boethius, tr. H. R. James (1897) · 56 short units / 5 books
- **Discourses of Epictetus (Selection)** — tr. George Long (1877) · 98 short units
- **Essays (First & Second Series)** — Ralph Waldo Emerson (1841, 1844) · 36 short units
- **Gulistan — The Rose Garden** — Saadi, tr. James Ross (1823) · 67 short units
- **The Works of Mencius** — tr. James Legge (1895) · 134 short units / 7 books
- **On Duties (De Officiis)** — Cicero, tr. Walter Miller (1913) · 86 short units / 3 books
- **Pensées** — Blaise Pascal, tr. W. F. Trotter (1910) · 181 short units
- **Pirkei Avot (Ethics of the Fathers)** — tr. Joseph I. Gorfinkle (1913) · 26 short units
- **Politics** — Aristotle, tr. William Ellis (1776) · 149 short units / 8 books
- **The Republic** — Plato, tr. Benjamin Jowett (1871) · 27 short units / 10 books
- **Walden** — Henry David Thoreau (1854) · 33 short units
- **The Writings of Zhuangzi (Chuang Tzu)** — tr. James Legge (1891) · 179 short units

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
