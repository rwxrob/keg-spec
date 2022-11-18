# Node identifier

* A KEG **node** MUST have an identifier that is unique to the keg containing the node.
* A **node identifier** MUST NOT change when a node **title** changes.
* A node identifier MUST be an incremental integer starting at 1.
* A node identifier MUST NOT be reused when previously published content is deleted.
* A node identifier MUST be included in the **nodes index file**.

Integer node identifiers make ridiculously short URLs when publishing to the **KEG Web**.

```
https://rwx.gg/45
rwx.gg/45
```

Node identifiers are modeled after primary keys in most database systems. Importing a node into a database is therefore rather trivial when the need arises.

The simplicity and size of an integer identifier solves unanticipated problems such as posting KEG Web URLs to forums and social media applications with limitations on length.

Numbers are easy to remember, take very little space, and are guaranteed not to break when the title changes. Creating a new node is trivial using this method.

```
cd $KEG
mkdir 2
vi 2/README.md
```

* [Beautiful simplicity of Luhmann's identifiers](/4)
* [Tim Berners-Lee warned against "slugs" in the 90s](/2)
