# Last changes index

* A **keg** MAY have an **index node** with `dex` ID containing last node changes.
* Content creators SHOULD provide a last changes index.
* Index `dex` content is specified and ID reserved.
* Index MAY use any title.
* Index MAY include one **paragraph block** before list.
* Index MUST contain a list with one list item for every KEG node.
* List item MUST contain a single KEGML **node link**.
* List item MUST begin with an **isosec** of second node last changed.
* Last change MUST be determined by changes to *any* file in node.
* List MUST be sorted by isosec.
* Index MUST be listed in **keg info file**.

A special reserved index is specified to contain a list of all nodes with the last changed nodes at the top of the list. The node ID `dex` is therefore reserved and unavailable to content creators. If a content creator chooses to provide a `dex`, however, then it must be listed in the keg info file along with any other custom indexes provided.

```md
# Last Changes Index

This index is automatically updated when new content is created or old content is updated. The latest changes are always on top. Every KEG content node is included. This list is guaranteed to always be the first and only list so that it can be reliably used to compare to previous cached copies of this KEG site to determine what has been updated.

* 20221031180218 [KEG nodes index file](/3)
* 20221031180317 [Beautiful simplicity of Luhmann's identifiers](/4)
* 20221031180345 [Much newer than others, after one with no title](/300)
```
