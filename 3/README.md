# KEGNODES index file

* A file named `KEGNODES` MUST exist in the KEG root directory.
* `KEGNODES` file MUST contain one line for every KEG node.
* `KEGNODES` MUST use standard UTF-8 encoding.
* `KEGNODES` MUST NOT contain blank lines.
* `KEGNODES` MUST use line-feed (`\n`) only to end lines.
* A `KEGNODES` line MUST contain three initial fields: **isosec**, **type**, **identifier**.
* A `KEGNODES` line MAY contain any valid KEG node title after first three fields.
* A `KEGNODES` line MUST be terminated by a single line feed (`\n`).
* `KEGNODES` fields MUST be separated by a single space.
* `KEGNODES` file MUST be sorted by first field (isosec).
* `isosec` MUST match the approximate second of last node update.
* `isosec` MUST NOT contain a `T`.
* `type` MUST be one of `t`, `d`, `f`, `D`, `g`, `G`, `F`, `T`, `R`.
* `t` MUST be reserved for "text"
* `d` MUST be reserved for "data"
* `f` MUST be reserved for "figure"
* `D` MUST be reserved for "data, text" (ex: data with explanatory text)
* `g` MUST be reserved for "data, figure" (ex: data displayed as figure)
* `G` MUST be reserved for "figure, data" (ex: figure derived from data)
* `F` MUST be reserved for "figure, text" (ex: figure with commentary)
* `T` MUST be reserved for "text, figure" (ex: text with illustration)
* `R` MUST be reserved for "text, data, figure" (ex: rich, equal priority)
* `identifier` MUST be an integer without leading zeros.

Note in this sample that the fields are very easily sorted and searched and that the title is entirely optional (but recommended to facilitate searches).

```kegnodes
20221031180218 t 3 KEGNODES index file
20221031180317 D 4 Beautiful simplicity of Luhmann's identifiers
20221031180317 R 5
```

Creating and maintaining a `KEGNODES` file takes nothing more than paper, pencil, and an accurate watch.

Creating a `KEGNODES` initially (with all text types `t`) is trivial from any modern UNIX shell because the KEG directory already contains most of the index information.

```
while read -r readme; do
  id=${readme%/README.md}
  echo "$(date -r "$readme" -u +%Y%m%d%H%M%S ) t $id $(head -1 $readme)"
done < <(ls -1 */README.md )
```

After generating a file in this way it can be updated by hand by simply changing the isosec values and types and titles as needed and resorting the file.
