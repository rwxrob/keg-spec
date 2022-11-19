# Last changes index

* A **keg** MAY have an **index node** with `dex` ID.
* Content creators SHOULD provide a last changes index.
* Index `dex` content is specified and ID reserved.
* Like any **index** MUST be listed in **keg info file**.

A special reserved index is specified to contain a list of all nodes with the last changed nodes at the top of the list. The node ID `dex` is therefore reserved and unavailable to content creators. If a content creator chooses to provide a `dex`, however, then it must be listed in the keg info file along with any other custom indexes provided.
