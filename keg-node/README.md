# KEG Node

Also known as a "knowledge node" or just "node". The term *node* comes
form the graph data structure and mathematics. A node is the vertex at
which other lines, links, or edges meet. It is the most granular
and composable unit of the KEG network.

A KEG *node* is simply a directory that MUST contain one of the
identifying structured content files.

* Text - `README.md`
* Data - `DATA.*`
* Figures - `FIGURE.*`

The asterisk current represents the following possible structured data
formats (only):

* `yaml` - simplified YAML with merge operator (but no remote linking, etc.)
* `json` - JSON (included for specificity)
* `csv` - proper MS CSV format (not just comma delimited)
* `tsv` - tab delimited (and only tabs)
* `toml` - Tom's Obvious Minimal Language (includes INI)
* `properties` - Java (originally) properties file

There are only three major types of knowledge nodes, and three is all
there will ever be. This limitation is intentional.

These types can easily be represented in printed form. This is the
guiding design principle for relevant content on the Knowledge Exchange
Grid. Anything else can certainly be referred to from KEG content, just
hosted elsewhere, on a network work appropriate for such content.

No other major node types will ever be considered for future KEG
specification versions.

The *node* `README.md` file MUST be valid KEG Markdown to be considered
a *node* at all. Invalid `README.md` files MUST disqualify the *node*
and its containing KEG Directory from any exchange over the KEG network.
This strict requirement ensures consistent semantic searches will
produce expected results.

A *node* directory (not to be confused with a KEG *Directory*) MAY
contain any other files including a *generator* script.

All files within a *node* --- including any beginning with dot or
underscore --- MUST be considered a part of the *node* and travel with
it when cloned or cached. This ensures that anyone or anything
replicating a node can always do so safely (without otherwise
eliminating certain files from the replication).

:::warn
Never include secrets or "hidden" files of any kind within any
*knowledge node*.
:::

A *node* MUST NOT contain other nodes.

A *node* MUST belong (be contained within) a *directory*.

A *node* MAY belong to several *directories* through hard or soft
linking.

* [Dynamic Nodes](/dynamic-node)
* [KEG Text Nodes](/text-node)
* [KEG Data Nodes](/data-node)
* [KEG Figure Nodes](/figure-node)
