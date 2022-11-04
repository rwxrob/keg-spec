# KEGNODES Manifest File

The `KEGNODES` manifest file MUST contain one line for every KEG node
--- including [secondaries](/secondary-nodes) and
[orphans](/orphan-nodes).

The file MUST contain simple text (standard UTF-8 encoding).

The file MUST NOT contain any blank lines.

The file lines MUST contain three fields (only) separated by a single
space: isosec, type, id

The file lines MUST end with line return optionally preceded by a
carriage return.

The file MUST be sorted by the first field (isosec).

The first field MUST be an [isosec unique identifer](/isosec)

The second field MUST be one of the following to indicate the [KEG node
type(s)](/schema-node).

* `t` - text
* `d` - data
* `f` - figure
* `D` - data, text (ex: table data within text)
* `g` - data,figure (priority on data, but figure from data)
* `G` - figure, data (as in "graphic", priority on figure over data)
* `F` - figure, text (priority on figure, ex: art with commentary)
* `T` - text, figure (ex: story with illustration(s))
* `R` - text, data, figure  (rich, text, data, figures, equal priority)

The third field MUST be a [KEG node identifier](/schema-node). Any
identifier is allowed but it is strongly RECOMMENDED that identifiers
match the "slug" of the title.

KEG node identifiers MUST be constant and SHOULD match the title of the
node. KEG node content, however, may change any time. Content creators
are therefore motivated to create titles that promote the discussion of
a topic of change to that content if there is a change. Otherwise, the
node should be deleted and replaced, or deprecated (forced orphan no
longer in KEGNODES), and updated to point to something new if
appropriate. Those following such a node can easily see if and when a
node becomes deprecated because they will still likely have the cached
deprecated copy. It is up to them to discard it or not. This strongly
dispels the illusion that content produced anywhere on the Internet is
not, in fact, eternal and should promote more introspection before
posting anything, and honestly from those who would retract what they
write and share..

Here's a sample from this KEG (`keg-spec`):

```kegnodes
20221031180218 t kegnodes-file
20221031180317 D schema-keg
```
