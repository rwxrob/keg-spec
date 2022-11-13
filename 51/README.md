# KEGML Reference Links

A **reference link** is text that refers to another node or file within the current keg. The text is **bracketed** and that same bracketed text followed by a colon, a space, and the target node or file is included in a **reference block** anywhere in that same `README.md` file.

```kegml
This is a paragraph with a reference link pointing to a [node].

[node]: /some-node

Here is another ref link pointing to a [local file].

[local file]: some-file.txt

And another pointing to a [local node] within this node directory.

[local node]: local-node-dir-with-own-readme

```
