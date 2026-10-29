# glotmode-lexicon

The open-dictionary data behind [Glotmode](https://glotmode.kojones.org): one read-only SQLite file
per language, published as release assets. The app pins each file by SHA-256 and downloads it at
build time. Glotmode's code lives elsewhere; this repository only holds the data.

## Releases

| Release | Language | Built from |
|---|---|---|
| `de-v1` | German | kaikki.org's Wiktextract extract of English Wiktionary (German entries), 2026-10-25 |

## Attribution and license

The lexicon is built from **[Wiktionary](https://www.wiktionary.org/)** content, extracted by
**[Wiktextract](https://github.com/tatuylonen/wiktextract)** and published on
**[kaikki.org](https://kaikki.org/)**. © Wiktionary contributors.

Wiktionary's text is available under the
[Creative Commons Attribution-ShareAlike 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
license (and the [GFDL 1.1+](https://www.gnu.org/licenses/fdl.html)). These lexicon files are an
adaptation and are released under **CC BY-SA 4.0** as well.

**What was changed:** the entries were filtered and reformatted for Glotmode. Proper names,
affixes and symbols were dropped. Each part-of-speech heading became one entry, keeping its English
glosses in source order, the noun gender, plural and genitive, the verb principal parts and
auxiliaries, and the adjective comparison. A form → lemma table was derived from the inflection
tables and form-of entries.
