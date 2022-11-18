# Node reference

* A **node reference** MUST be a slash (`/`) followed by an integer and optional **query code**.
* A node reference MUST occur within a **link target**.
* A node reference MUST refer to an existing **node** in keg **nodes index file**.
* A node reference MAY refer **node zero** while waiting for it to be created.
* A **KEG app** MUST fail to operate until any invalid node reference is corrected.
