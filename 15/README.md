# KEG directory

A KEG directory (also referred to as a "keg site" or just "a keg") MUST contain one or more [KEG nodes](/keg-node), each with a uniquely identifying directory name within the KEG directory itself.

A KEG directory itself fulfills the requirements for a KEG *node* except for the obvious exception that it MUST contain other nodes (where normally a *node* may not).

A KEG directory MUST contain a `KEG.yaml` file.

A KEG directory MUST contain a KEGNODES file.

A KEG directory MAY contain an FOLLOW file with URLs of KEGs to cache and follow.

A KEG directory MAY contain an AVOID file with URLs of KEGs to blacklist and avoid.

A KEG directory may contain any number of other files, but SHOULD avoid large files.

* [KEGNODES Manifest File](/kegnodes-file)
* [KEG Directory Schema](/schema-keg)
