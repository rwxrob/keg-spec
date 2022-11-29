# Node

* A node MAY contain additional **unlinked files**.
* A **KEG app** MUST observe reservation of `README.md` file.
* A keg app MUST observe reservation of `meta` file.
* A node MAY contain any number of additional files and directories.
* A node MUST NOT contain other *node* directories (but regular directories are fine).
* A node MUST NOT contain any secret files.
* A node MUST be in a keg directory to be considered a node.
* A potential node MAY exist outside of a keg awaiting eventual import into a valid keg.
* A node MAY be moved to another keg simply by renaming the directory and path.
* A migrated node MUST appear as a new node in the target keg with new relative node ID.
* A KEG app MAY clone one or more nodes from one keg into another.

A KEG node (aka "content node", "knowledge node", or just "node") is simply a directory that contains a **README.md** file written in **KEGML**, an optional **meta matter** file, and any number of other files or directories provided none of them are considered nodes themselves by an KEG app.

A node is the most granular and composable unit of KEG. The name derives comes from "graph node" in a **graph data structure** where the node is a vertex at which other lines, links, or edges intersect.

* [*Dynamic Nodes](../11)
* [*Text Nodes](../0)
* [*Data Nodes](../0)
* [*Figure Nodes](../0)
* [*Graphic Nodes](../0)
