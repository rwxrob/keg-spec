# Nodes index file

* A file named `dex` MUST exist in the KEG root directory.
* The index MUST contain one line for every KEG node.
* File MUST use standard UTF-8 encoding.
* File MUST NOT contain blank lines.
* File MUST use line-feed (`\n`) only to end lines.
* Lines MUST contain three initial fields: **isosec**, **type**, **identifier**.
* Lines MAY contain any valid KEG node title after first three fields.
* Creators and apps SHOULD start titles on same line column for easy reading.
* Lines MUST be terminated by a single line feed (`\n`).
* Lines MUST be separated by a single space except after third field.
* After the third field 1-8 spaces are allowed to facilitate title alignment.
* File MUST be sorted by first field (isosec).
* Field 1 (isosec) MUST match the approximate second of last node update.
* Field 1 (isosec) MUST NOT contain a `T` or any other punctuation (20060102030405).
* Field 2 (type) MUST be one of `t`, `d`, `f`, `g`.
* Type `t` MUST be reserved for "text"
* Type `d` MUST be reserved for "data"
* Type `f` MUST be reserved for "figure"
* Type `g` MUST be reserved for "graphic" (ex: data displayed as figure)
* Field 3 (identifier) MUST be an integer without leading zeros.

Note in this sample that the fields are very easily sorted and searched and that the title is entirely optional (but recommended to facilitate searches).

```kegnodes
20221031180218 t 3   KEG nodes index file
20221031180317 g 4   Beautiful simplicity of Luhmann's identifiers
20221031180304 t 5
20221031180345 t 300 Much newer than others, after one with no title
```

Creating and maintaining an `index` file takes nothing more than paper, pencil, and an accurate watch.

Creating an `index` initially (with all text types `t`) is trivial from any modern UNIX shell because the KEG directory already contains most of the index information.

```
while read -r readme; do
  id=${readme%/README.md}
  echo "$(date -r "$readme" -u +%Y%m%d%H%M%S ) t $id $(head -1 $readme)"
done < <(ls -1 */README.md )
```

After generating a file in this way it can be updated by hand by simply changing the isosec values and types and titles as needed and resorting the file.
