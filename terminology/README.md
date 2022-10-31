# Terminology

Here is brief summary of the terms used in this specification. Longer,
detailed definitions --- including formal schemas --- are included
later.

A ***node*** (or "knowledge node") is simply a directory with a
`README.md` or `DATA.*` file in it.

A ***dynamic node*** (or "generated node") is a *node* that requires a
generator be run to produce the `README.md` or `DATA.*` files.

A * and any number of optional source
files from this these other two main files are generated. This
simplicity is by design. A *node* is
considered *static* if it does not have a generator. If it does, it's
considered *dynamic*.

***directory***
***site***
***slug***
***isosec***

A ***text node*** contains only KEGMark text.

A ***collection node*** is a *text node* that includes one or more
*bulleted import lists*.

A ***composite node*** is a *dynamic node* that is generated from other
nodes. A book is an example of a *composite node*.

A ***bulleted import list*** is a KEGMark block type consisting of a
regular bulleted list with nothing but links for items in the list. When
browsing from are rendered Web version or GitHub clicking on any of the
links in the list will open the knowledge source file. But, such lists
can also easily be expanded into larger *composite nodes* by simply
replacing the bullet list item with the content of the link target. Any
headers in the imported content will be incremented by one (prefixed
with a single, additional hashtag `#`).

An ***isosec*** is the GMT current time in ISO8601 (RFC3339) without any
punctuation or the T.

```
20060102030405
```

This unique identifier is preferred over others since it can easily be
determined with nothing more than a watch or wall clock with a second
hand.

* [Formerly Known As](/formerly-known-as)
