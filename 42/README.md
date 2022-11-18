# KEGML differences from Markdown

The KEGML design contains many significant constraints from both Pandoc and the original Markdown out of necessity and to address glaring omissions. The strictness of these limitations is very much by design since they produce the simplest, most compatible knowledge source capable of being represented in any number of ways through rendering later.

* Paragraphs must never contain single line returns (soft wraps)
* Paragraphs may contain hard wraps (two or more trailing spaces)
* No escaping anything with backslash at all
* Only node links and footnote refs in paragraphs for easier reading
* No URLs allowed in anything but a footnote and list item
* Only printable UNICODE code points and simplified white-space allowed
* White-space consists of `space` or `newline` only
* Carriage returns (`\r`) are not allowed
* Blocks delimited with one or more blank lines
* A *blank line* is any line containing only white space
* No headings allowed except for **title**
* Title must not exceed 72 runes including the `# ` prefix
* No `heading` attributes
* Use of double prime (`"`) and (`'`) required for quotes
* No smart punctuation specified (up to renders)
* Include node link: `* [Some Title](/23)`
* Include file link: `* [Some File](file.yaml)`
* Nodes must be included at that location with that title
* Files must be included with title exactly as they with suffix as class
* Limited footnote support (from Pandoc)
* Footnotes have no line returns (link to node if need more)
* No "front matter" allowed
* No HTML nor raw Latex 
* Only `division` allows inclusion of other blocks
* Full support for Pandoc *regular* attributes (only, no "raw attributes)
* Only `verbatim`, `bracketed` span and `division`, `fenced` blocks support attributes
* Undotted single class attributes should be preferred
* Languages must use the `{lang=en}` standard semantic attribute notation
* A list of standardized attributes will be included with KEG (superset of Pandoc)
* Non-semantic attributes are strongly discouraged since they destroy readability
* Both `BACKTICK{3,8}` and `SQUIGLE{3,8}` supported for `fenced`
* Languages should generally be separated by blocks --- especially `div`
* A single space is optional between opening `division` and `fenced` token
* Div blocks should take advantage of initial cap readability `::: Warning`
* Div block opening just be followed by blank line
* Div block closing must be preceded by blank line
* A `verbatim` span must never contain a backtick (use `bracketed`, etc. instead)
* Spans composed of `fields` of printable UNICODE code points
* Fields are composed of `words`
* Only one Refs block for a single KEG node (and it must be above tags)
* Fields composed of `letters`, `punc`, `printable` (hyphenated terms, etc.)
* Only GitHub flavored tables supported
* Only four dashes for separator (`----`)
* A list item is paragraph with list item prefix (single line)
* Lists focused on creating outlines
* No extended (long) lists
* Apps should convert long ("em") dashes `---`
* Apps should convert ("en") dashes `--`
* Apps should convert ellipsis `...`
* No tabs whatsoever, not even optional white space or `raw` (use file
  include instead)
* No HTML (not even for "comments")
* Images limited to own block
* Full inline and block MathJax
* Multiple images supported, but should be not be too bulky and provide value.
* Call an image a **figure** instead (and treat it like one).
* All image content must be fully described and have alt text description for appendix.
