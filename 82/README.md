# Meta matter

* **Front matter** MUST NOT appear in any KEGML document.
* A **KEG app** MUST flag front matter as a critical syntax error.
* A **node** MAY include a **meta matter** file named `meta` instead.
* Meta matter MUST be **simplified YAML**.

Meta matter is similar to "front matter" except it isn't included in **README.md** file where it would distract from the source content during the writing process. This also allows meta matter files to be automatically updated and queried without having to first parse them from the README.md file. This ensures that the KEGML **title** is *always* the first line of any **node**.

Meta matter also uses a simpler and safer form of YAML that is essentially JSON as YAML. Since the content of the `meta` file can be either JSON or YAML and because few can agree on the `.yml` or `.yaml` suffix the suffix has simply been omitted. This also makes for cleaner URLs when pushed to the **KEG Web**.

* [Sample README.md with meta matter](sample-meta-matter.md)
* ["Front matter" fails.](/83?L)
* [Doesn't meta matter at the end slow parsing?](/107?L)
