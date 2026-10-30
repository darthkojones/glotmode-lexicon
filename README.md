# glotmode-lexicon

The open-dictionary data behind [Glotmode](https://glotmode.kojones.org): one read-only SQLite file
per language, published as release assets. The app pins each file by SHA-256 and downloads it at
build time. Glotmode's code lives elsewhere; this repository only holds the data.

## Releases

| Release | Language | Built from |
|---|---|---|
| `de-v1` | German | kaikki.org's Wiktextract extract of English Wiktionary (German entries), 2026-10-25 |
| `es-v1` | Spanish | the same, Spanish entries, 2026-10-25 |
| `it-v1` | Italian | the same, Italian entries, 2026-10-25 |
| `de-v2` | German | as `de-v1`, plus synonyms from Wiktionary and [OpenThesaurus](https://www.openthesaurus.de/) (text version of 2026-10-29) |
| `es-v2` | Spanish | as `es-v1`, plus Wiktionary synonyms |
| `it-v2` | Italian | as `it-v1`, plus Wiktionary synonyms |

## Attribution and license

The lexicon is built from **[Wiktionary](https://www.wiktionary.org/)** content, extracted by
**[Wiktextract](https://github.com/tatuylonen/wiktextract)** and published on
**[kaikki.org](https://kaikki.org/)**. © Wiktionary contributors.
From `de-v2`, German synonyms also come from **[OpenThesaurus](https://www.openthesaurus.de/)**
(© Daniel Naber and contributors; data under CC BY-SA 4.0 or LGPL — used here under CC BY-SA 4.0).

Wiktionary's text is available under the
[Creative Commons Attribution-ShareAlike 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
license (and the [GFDL 1.1+](https://www.gnu.org/licenses/fdl.html)). These lexicon files are an
adaptation and are released under **CC BY-SA 4.0** as well.

**What was changed:** the entries were filtered and reformatted for Glotmode. Proper names,
affixes and symbols were dropped. Each part-of-speech heading became one entry, keeping its English
glosses in source order, the noun gender, plural and genitive, the verb principal parts and
auxiliaries, and the adjective comparison. A form → lemma table was derived from the inflection
tables and form-of entries. Italian forms are respelled without Wiktionary's stress marks (fàccio →
faccio), and verbs with attached pronouns (comprarselo, dámelo) became form → lemma rows. From v2, each
entry keeps synonyms from its first three meanings (Wiktionary) and, for German, OpenThesaurus
synonym sets in which the word appears plainly, on entries whose part of speech is unambiguous.
