# KEGML Differences from Markdown

Here's a rough summary of KEGML syntax related to other Markdown
versions:

* Only printable UNICODE code points and simplified white-space allowed
* White-space consists of `space` or `newline` only
* A `newline` is always a `\n` optionally preceded by a `\r`
* Blocks delimited with one or more blank lines
* No headings (`title` is it's own block, and must be first)
* Blocks: `include`, `paragraph`, `bulleted`, `numbered`, `figure`, `title`,
  `syntaxed`, `verbatim`, `tex`, `quote`, `semantic`, `tags`
* Spans: `plain`, `em`, `strong`, `stremph`, `del`, `math`, `sem`
* The `tags` block is a Markdown `verbatim` but must be last
* Only `semantic` and `quote` allows inclusion of other blocks
* The `quote` is exactly equivalent to `semantic` with "quote" class
* Hard line breaks are multiple space
* A `newline` is ignored `paragraph`, `bulleted`, `numbered`,
* Only `semantic`, `syntaxed` blocks, and `sem` span support classes
* Classes are limited to single words (no key-value attributes)
* No space allowed between initial token and blocks with classes
* All spans and blocks must be semantic (like HTML5 `<i>`, `<b>`)
* Spans composed of `fields` of printable UNICODE code points
* Fields composed of `letters`, `punc`, `printable` (hyphenated terms, etc.)
* No tables (better as DATA node instead)
* No nested spans
* No separators
* No nested list items
* No extended (long) lists
* No HTML (not even for "comments")
* Images limited to own block
* Full support for inline and raw LaTeX and MathJax
* Unspecified title-to-id (slug) conversion

**Images MUST NOT be included in KEGML.** Unlike most other flavors
of Markdown, KEGML deliberately omits images of any kind. This is
because all images MUST be contained within their own *figure nodes*.
This promotes the use of images to convey something that cannot
otherwise be described with text. Such a limitation promotes the widest
possible range of participants and eliminates superfluous decoration
which bloats content and complicates the publishing process.

