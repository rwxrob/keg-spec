# KEG Node

The term **KEG node** (aka "knowledge node" or "node") comes from a **graph data structure** in which a **graph node** is the vertex at which other lines, links, or edges meet. There are different types of graphs including a **rooted node tree** which takes the form of a top-down hierarchy commonly found in a document table of contents or file directory structure. The Web and social media networks are non-hierarchical graphs where the more links to a given node create a greater weight. This is how the basic idea behind search engine optimization, for example.

A **keg** is  rooted node tree and a **node** is a unit of knowledge content that optionally refers (and/or includes) other nodes.

Every **keg** is a graph data structure where each node contains knowledge content. A collection of kegs is also a graph data structure where the individual kegs each become a branch of a larger graph data structure.

It is the most granular and composable unit of the KEG network.

A KEG node is simply a directory that MUST contain one of the identifying structured content files.

* Text (T) - `README.md`
* Data (D) - `DATA.*`
* Figure (F) - `FIGURE.*`

These file names are reserved for use by KEG. These types (and combinations of these types) are represented by a single character in the [KEGNODES manifest file](/kegnodes-file).

There are only three major types of knowledge nodes, and three is all there will ever be. This limitation is intentional.

A KEG node may have multiple types simultaneously. For example, a data node might also be a figure node containing a graph that is dynamically generated from the DATA.* file, and both the data and the figure might be included in the README.md file of the same node as type text. 

The asterisk current represents the following possible structured data formats (only):

* `yaml` - simplified YAML with merge operator (but no remote linking, etc.)
* `json` - JSON (included for specificity)
* `csv` - proper MS CSV format (not just comma delimited)
* `tsv` - tab delimited (and only tabs)
* `toml` - Tom's Obvious Minimal Language (includes INI)
* `properties` - Java (originally) properties file

A node directory (not to be confused with a [KEG directory]) MAY contain any other files including a *generator* script.

::: Warning

While such files are not involved in KEG exchange and caching unless the are
linked, they should nevertheless not be considered secret. Never include
secrets or "hidden" files of any kind within any *knowledge node*.

:::

A node directory MUST NOT contain other node directories (but can include and link to them from the README.md file).

A node MUST be contained within a KEG directory to be considered a node. Node directories can, however, exist outside of a KEG directory as orphans or drafts awaiting migration into a KEG directory.

A node MAY be freely moved to other KEGs simply by moving the node directory into the other KEG directory and update both KEGNODES files. In fact, this is encouraged and well supported to facilitate better use of KEGs as categories until themselves.

A *node* MAY belong to several *directories* through hard or soft linking. Replication and syncing, however, are very much preferred to preserve the truly static nature of the KEG content.

* [Dynamic Nodes](/dynamic-node)
* [KEG Text Nodes](/text-node)
* [KEG Data Nodes](/data-node)
* [KEG Figure Nodes](/figure-node)
