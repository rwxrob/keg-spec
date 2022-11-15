# Optional index nodes

Optional indexes of different kinds of KEG content allow a **content creator** or **follower** to easily search the content based on whatever semantic meaning has been applied to the limited number of KEGML types. Followers may choose to omit the optional index nodes from their own personal caches of kegs they follow.

* An **index node** is an optional **keg data node** with a special ID.
* An **index node** ID MUST match the plural of **KEGML content type** contained.
* The **title** of the **index node** MAY be any valid title.
* Content creators MAY assign semantic meaning to **KEGML content types**.

While the `dex` file does contain all keg titles. It is sometimes desirable to have a `titles` index node as well to present that content in more consumable, render-able ways. For example, when rendering an `index.html` file for each `README.md` file in every node.

In most cases, an index node will have both a `data.*` file and a rendered `README.md` file (and some people will included an `index.html` file as well).

Another example is a terminology index that maps to the `bold` type.

The [**zero node**](/59) can double as an index node containing all the nodes that link to it (instead of the content being planned).

For those wishing a comprehensive analysis of their keg content the frequently occurring `word` type could be mapped to a `words` index with a visually pleasing word map graphic.
