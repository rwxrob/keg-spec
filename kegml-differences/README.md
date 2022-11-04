# KEGML Differences from Markdown

The KEGML design contains many significant constraints from both Pandoc and the original Markdown out of necessity and to address glaring omissions. The strictness of these limitations is very much by design since they produce the simplest, most compatible knowledge source capable of being represented in any number of ways through rendering later.

* Paragraphs must never contain single line returns (soft wraps)
* Paragraphs may contain hard wraps (two line returns)
* No escaping anything with backslash at all (overcomplicates)
* Only reference links in paragraphs for easier reading
* Only printable UNICODE code points and simplified white-space allowed
* White-space consists of `space` or `newline` only
* A `newline` is always a `\n` (never preceded by a `\r`)
* Blocks delimited with one or more blank lines
* A *blank line* is any line containing only white space
* No headings (`title` is it's own block, and must be first)
* Title must not exceed 72 runes including the `# ` prefix
* Richer variation of spans including punctuated (brackets).
* Repurposed blocks as include lists
* Include node link: `* [Some Title](/node)`
* Include file link: `* [Some File](file.yaml)`
* Specified reserved suffixes: `md`, `yaml`, `json`, `csv`, `tsv`
* Nodes must be included at that location with that title
* Files must be included with title exactly as they are in a `semblk` with suffix
* Limited footnote support (from Pandoc)
* Footnotes have no line returns (link to node if need more)
* The `tags` block is a Markdown `raw` but must be last
* Only `semblk` and `quote` allows inclusion of other blocks
* Full support for Pandoc *regular* attributes (only, no "raw attributes)
* Only `verbatim`, `bracketed` span and `div`, `fenced` blocks support attributes
* Undotted single class attributes should be preferred
* Languages must use the `{lang=en}` standard semantic attribute notation
* A list of standardized attributes will be included with KEG (superset of Pandoc)
* Non-semantic attributes are strongly discouraged since they destroy readability
* Both `BACKTICK{3,8}` and `SQUIGLE{3,8}` supported for `fenced`
* Languages should generally be separated by blocks --- especially `div`
* A single space is optional between opening `div` and `fenced`
* Div blocks should take advantage of initial cap readability `::: Warning`
* No `heading` attributes
* A `verbatim` span must never contain a backtick (use `bracketed`, etc. instead)
* All spans are semantic (like HTML5 `<i>`, `<b>`, think novels)
* Spans composed of `fields` of printable UNICODE code points
* Fields composed of `letters`, `punc`, `printable` (hyphenated terms, etc.)
* No tables whatsoever (better as DATA node instead)
* No separators (horizontal rules)
* No nested list items
* No extended (long) lists
* Long ("em") dashes `---`
* Short ("en") dashes `--`
* Ellipsis `...`
* No tabs whatsoever, not even optional white space or `raw` (use file
  include instead)
* No HTML (not even for "comments")
* Images limited to own block
* Full support for inline and raw LaTeX and MathJax
* Unspecified title-to-id (slug) conversion

**Images MUST NOT be included in KEGML.** Unlike most other flavors of Markdown, KEGML deliberately omits images of any kind. This is because all images MUST be contained within their own *figure nodes*. This promotes the use of images to convey something that cannot otherwise be described with text. Such a limitation promotes the widest possible range of participants and eliminates superfluous decoration which bloats content and complicates the publishing process.

