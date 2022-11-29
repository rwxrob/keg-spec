# ID vs title

There's a strong distinction between a *keg node ID* and a *keg node title*. It is very [important](../2) that content creators and tool developers fully understand this.

* A title MUST be the first-line of text in any KEGML node `README.md` file.
* An ID MUST be the unique integer directory name containing the `README.md` file.
* An id MUST NOT change and can only be deleted.
* An id MUST NOT be replaced if deleted.
* A title SHOULD be readable and human-friendly but can be any valid KEGML title.
* A title MUST be able to be freely changed.
* A title SHOULD continue to represent the general topic when and if changed.

This flexibility allows content creators to change their content and explanations, even make 180 turns in conclusions and statements without breaking any link to that content, not just on KEG, but across the entire [Web](../2).
