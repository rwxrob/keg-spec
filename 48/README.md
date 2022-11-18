# KEG Info File

* A **keg** MUST include a `keg` YAML file known as the **keg info file**.
* File MUST be YAML v1.2+ format.
* File MAY be JSON (since JSON *is* YAML).
* File MUST NOT have external file dependencies.
* File MAY contain authoritative schema definitions.
* A **KEG app** MUST validate the file schema.
* The **info file schema** MUST be maintained in this specification.
* Schema MUST be on the **KEG Web**.[^48]
* Schema MUST never contain breaking changes.
* Schema MAY deprecate schema rules over time.

A KEG **info file** named `keg` (aka "keg file") identifies a **keg directory** and distinguishes it from other directories. When a **content creator** publishes a keg to the **KEG Web** this file also serves to identify KEG content to KEG Web crawlers.

* [Custom KEG info data](/7)
* [YAML Schema](keg.schema.yaml)
* [JSON Schema (from YAML)](keg.schema.json)

[^48]: The specification is itself a keg hosted on the KEG Web site https://spec.keg.pub/keg
