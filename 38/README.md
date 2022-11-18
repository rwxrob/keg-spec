# Query code

* Every **node** MUST have a **title**
* Every **include** MUST have **link text**.
* An **include link** MAY include a **query code**.
* A query code is also an HTML query string and may conflict with some host services.
* A query code MUST appear immediately after the **include link** **link target**.
* A query code MUST begin with question mark (`?`).
* A KEG reserved query code continues until the first comma (`,`) or end.
* A **KEG app** MUST NOT define any query code *before* the first comma.
* A KEG app MAY use query codes by appending after a comma (`,`).
* A KEG app MAY use any combination of *lower case* ASCII alpha-numeric runes.
* No query code means that **link text** must become relative **heading**.
* `T` code means target title must become heading (instead of link text).
* `L` code means link text MUST become **lede** (and not heading).
* `0` code means both link text and target title should be ignored.

Here is the list of currently supported and encouraged query codes. As more materialize they will be added here in subsequent versions of the KEG **specification**:

Query Code | Behavior
-|-
(none) | Link text becomes relative heading (beginning with hashtags `#`)
T      | Target title becomes relative heading
L      | Link text becomes lede
0      | Link text and title are ignored
