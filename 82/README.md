# Meta matter block

* A KEGML **node** README.md file MAY contain a final **meta matter block**.
* **Meta matter** MUST be considered a part of the actual KEGML document model.
* **Meta matter** MUST be indented four spaces.
* **Meta matter** MUST NOT contain any blank lines.
* **Meta matter** MUST be **simplified YAML** (including JSON).
* **Meta matter** MAY be followed by optional (accidental) white space.
* **Meta matter** MUST not be abused when a **file include link** would work better.
* **Meta matter** MUST only contain data about the node containing it.

KEGML disposes of "front matter" and replaces it with the more appropriately named and positioned **meta matter** at the end of the README.md file as **simplified YAML** (which includes JSON if you really like) inside a **raw block**.

* [Sample README.md with meta matter](sample-meta-matter.md)
* [*"Front matter" fails.](/83)
