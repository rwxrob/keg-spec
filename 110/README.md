# Search implementation suggestions

* Content creators are not required to provide any indexing at all.
* Content creators MAY provide specified indexing in `dex`.
* Content creators MAY provide custom indexing in other nodes.
* This **specification** MUST NOT require any search implementation.
* Specified indexes MUST be within `dex`.
* A **KEG app** SHOULD implement full text searching.
* App SHOULD allow configurable search optimizations.
* App SHOULD allow setting language-specific stop words.
* App SHOULD allow boolean[^110.1] search: `OR`, `|`, `||`, `AND`, `&&`, `&`, `(`, `)`.
* App SHOULD implement glob strings for partial words (like `find`).
* App SHOULD implement Go-compatible regular expression searching.
* App SHOULD provide dynamic, automatic words index creation.
* App SHOULD create `dex/nodes.md` and `dex/nodes.json` **last changes index**.
* App SHOULD create `dex/words.md` and `dex/words.json` indexes.
* App SHOULD create `dex/beacons.md` and `dex/beacons.json` indexes.
* App SHOULD create `dex/inflects.md` and `dex/inflects.json` indexes.
* App SHOULD create `dex/figures.md` and `dex/figures.json` indexes.
* App SHOULD create `dex/footnotes.md` and `dex/footnotes.json` indexes.
* App MAY create missing indexes within `dex` if observing this specification.
* App MUST NOT overwrite indexes already created in `dex`.

Given the relatively small size of a keg **node** (with only the one title heading) the need for search indexing beyond the **last changes index** is secondary. However, using tools like `grep` for full text searching is less than optimal when combining searches across all of a person's followed KEG site cached content. Therefore, creating a **words index** seems advantageous in the long run, even if the creator of the index isn't the content creator, but those following that creator. Having a common convention for searching across all of KEG provides obvious benefit when considered in this way.

[^110.1]: Karch, Marziah. "How to Do a Boolean Search in Google" (2021, Jan 2). *Lifewire*. https://www.lifewire.com/boolean-search-terms-google-1616810
