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

The third field MUST be one of `T` (text), `D` (data), `F` (figure) to
indicate the [KEG node type](/schema-node). This must indicate the
primary type when a secondary type is also allowed (data nodes that are
also figures because of dynamically generated graphs, etc.).

