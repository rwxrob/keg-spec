# KEG index file

* A file named `dex` MUST exist in the KEG root directory.
* The index MUST contain one line for every KEG node.
* File MUST use standard UTF-8 encoding.
* File MUST NOT contain blank lines.
* Lines MUST contain two initial fields: **isosec**, **keg identifier**.
* Lines MAY contain any valid KEG node **title** after first two fields.
* Lines MUST be terminated by a single line feed (`\n`).
* Fields MUST be separated by a single space.
* File MUST be reverse sorted by first field (isosec).

Note in this sample that the fields are very easily sorted and searched and that the title is entirely optional (but recommended to facilitate searches).

```kegnodes
20221031180218 3 KEG nodes index file
20221031180317 4 Beautiful simplicity of Luhmann's identifiers
20221031180304 5
20221031180345 300 Much newer than others, after one with no title
```

Creating and maintaining a `dex` file takes nothing more than paper, pencil, and an accurate watch but most choose to use a **keg app** to assist in the automatic updating of this file.

Creating an initial `dex` is trivial from any modern UNIX shell because the keg directory already contains most of the index information.

```
while read -r readme; do
  id=${readme%/README.md}
  echo "$(date -r "$readme" -u +%Y%m%d%H%M%S ) $id $(head -1 $readme)"
done < <(ls -1 */README.md ) | sort -r > dex
```

After generating a file in this way it can be updated by hand by simply changing the isosec values and types and titles as needed and resorting the file.
