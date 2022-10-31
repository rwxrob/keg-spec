# KEGNODES Manifest File

The `KEGNODES` manifest file MUST contain one line for every KEG node
--- including [secondaries](/secondary-nodes) and
[orphans](/orphan-nodes).

The file MUST contain simple text (standard UTF-8 encoding).

The file MUST NOT contain any blank lines.

The file lines MUST contain three fields (only) separated by a single
space: isosec, id, type.

The file lines MUST end with line return optionally preceded by a
carriage return.

The file MUST be sorted by the first field (isosec).

The first field MUST be an [isosec unique identifer](/isosec)

The second field MUST be a [KEG node unique identifier](/schema-node).

The third field MUST be one of the following to indicate the [KEG node
type(s)](/schema-node):

* `T` - text
* `D` - data
* `F` - figure
* `TD` - text, data (ex: table data within text)
* `DF` - data, figure (ex: data with graph)
* `TF` - text, figure (ex: art with commentary)
* `TDF` - text, data, figure  (ex: data with graph and explanation)

Here's a sample from this KEG (`keg-spec`):

```kegnodes
20221031180218 kegnodes-file T
20221031180317 schema-keg TD
```
