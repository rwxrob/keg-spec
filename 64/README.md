# Index node

* An **index node** (aka "index") is like a **node** but with a non-integer ID.
* ID MUST begin with an ASCII letter.
* ID MAY contain one or more ASCII letters, numbers, or hyphens after first letter.
* Hyphen MUST appear between two letters or digits.
* ID SHOULD be less 12 runes or less.
* ID SHOULD be easy to memorize.
* ID MUST NOT be `dex` unless as specified for KEG **last changes index**.
* Content creators SHOULD provide a `dex` index.
* Title MAY be any valid title.
* Index MAY contain any other block types before list block.
* Index MUST contain one and only one **list block**.
* List block MUST be last block.
* List block MAY also be an **include list**.
* List block MUST either be an include list or regular list block.
* **List item** MUST contain one and only one **node link**.
* List item MAY contain any other content in addition to node link.
* List block SHOULD be sorted somehow.
* Index MUST be listed in **keg info file** under `indexes` array with `id` and `summary` fields.

Optional indexes of different kinds of KEG content allow a **content creator** or **follower** to easily search the content based on whatever semantic meaning has been applied to the limited number of KEGML types. Followers may choose to omit the optional index nodes from their own personal caches of kegs they follow.

A [**zero node**](/59) can double as an index node containing all the nodes that link to it.

For those wishing a comprehensive analysis of their keg content the frequently occurring `word` type could be mapped to a `words` index with a visually pleasing word map graphic.

Those wishing to create top-level entry points into the keg content should use an include list instead of a simple list block. Such indexes can also be expanded into **KEGMLX** and eventually into full publications as well. In fact, depending on the method of hosting, having a fully expanded index as a PDF, ePub, or `index.html` within the index directory in addition to the mandatory `README.md` containing the include list is often recommended --- especially when other forms of content consumption are preferred (PDFs in a classroom, etc.).
