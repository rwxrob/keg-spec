# Info File

* A **keg** MUST include a `keg` file known as the keg **info file**.
* The **info file** MUST be YAML v1.2+ format.
* The **info file** MAY be JSON (since JSON *is* YAML).
* The **info file** MUST NOT have external file dependencies.
* The **info file** MAY contain authoritative schema definitions.
* A **keg app** MUST validate the **info file** schema.
* The **info file schema** MUST be maintained in this specification.
* The **info file schema** MUST be on Web at https://schema.keg.pub/keg
* The **info file schema** MUST never contain breaking changes.
* The **info file schema** MAY deprecate schema rules over time.

A KEG **info file** named `keg` (aka "keg file") identifies a **keg directory** and distinguishes it from other directories. When a **content creator** publishes a keg to the **KEG Web** this file also serves to identify KEG content to KEG Web crawlers.

* [Custom KEG info data](/7)
* [YAML Schema](keg.schema.yaml)
* [JSON Schema (from YAML)](keg.schema.json)
