# Node

* A **node** MAY contain additional **unlinked files**.
* A **node** MUST NOT contain any secret files.

The term keg **node** (aka "knowledge node" or "node") comes from a **graph data structure** in which a **graph node** is the vertex at which other lines, links, or edges meet. There are different types of graphs including a **rooted node tree** which takes the form of a top-down hierarchy commonly found in a document table of contents or file directory structure. The Web and social media networks are non-hierarchical graphs where the more links to a given node create a greater weight. This is how the basic idea behind search engine optimization, for example.

A **keg** is rooted node tree and a **node** is a unit of knowledge content that optionally refers (and/or includes) other nodes.

Every **keg** is a graph data structure where each node contains knowledge content. A collection of kegs is also a graph data structure where the individual kegs each become a branch of a larger graph data structure.

A node is the most granular and composable unit of KEG.

A node is simply a directory that contains a README.md file and one or more optional additional files depending on the **node type**.

Only the `README.md` file name is reserved for use within a node directory.

A node directory MUST NOT contain other node directories (but can include and link to them from the README.md file).

A node MUST be contained within a keg directory to be considered a node. A node directory can, however, exist outside of a keg directory awaiting eventual migration into a keg.

A node MAY be freely moved to other kegs simply by moving the node directory into the other keg's directory and updating the **nodes index file** in each keg.

A *node* MAY belong to several *directories* through hard or soft linking. Replication and syncing, however, are very much preferred to preserve the static nature of KEG content.

* [*Dynamic Nodes](/11)
* [*Text Nodes](/0)
* [*Data Nodes](/0)
* [*Figure Nodes](/0)
* [*Graphic Nodes](/0)
