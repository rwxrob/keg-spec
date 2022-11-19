# Index node

* An **index node** (aka "index") is an optional **node** with a non-integer ID.
* ID MUST begin with an ASCII letter.
* ID MAY contain one or more ASCII letters, numbers, or hyphens after first letter.
* Hyphen MUST appear between two letters or digits.
* ID SHOULD be less 12 runes or less.
* ID SHOULD be easy to memorize.
* ID MUST NOT be `dex` unless as specified for KEG **last changes index**.
* Content creators SHOULD provide a `dex` index.
* Index MUST contain **title**.
* Title MAY be any valid title.
* Index MUST contain one and only one **list block**.
* List block MUST be last block.
* Index MAY contain any other block types before list block.
* **List item** MUST begin with anything but **node link** (else **include list**).
* List item MUST contain one and only one **node link**.
* List block SHOULD be sorted somehow.
* Index MUST be listed in **keg info file** under `indexes` array with `id` and `summary` fields.

Optional indexes of different kinds of KEG content allow a **content creator** or **follower** to easily search the content based on whatever semantic meaning has been applied to the limited number of KEGML types. Followers may choose to omit the optional index nodes from their own personal caches of kegs they follow.

A [**zero node**](/59) can double as an index node containing all the nodes that link to it.

For those wishing a comprehensive analysis of their keg content the frequently occurring `word` type could be mapped to a `words` index with a visually pleasing word map graphic.
