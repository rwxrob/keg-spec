# KEG index file

* A file named `dex.md` MUST exist in the KEG root directory.
* The index MUST contain one line for every KEG node.
* File MUST use standard UTF-8 encoding.
* File MUST NOT contain blank lines.
* Each line MUST be a KEGML **node link**.
* Lines MUST contain an **isosec** to sort properly.
* File MUST be reverse sorted by first field (isosec).

Note in this sample that the fields are very easily sorted and searched and that the title is entirely optional (but recommended to facilitate searches).

```kegnodes
* 20221031180218 [KEG nodes index file](/3)
* 20221031180317 [Beautiful simplicity of Luhmann's identifiers](/4)
* 20221031180345 [Much newer than others, after one with no title](/300)
```

Creating and maintaining a `dex.md` file takes nothing more than paper, pencil, and an accurate watch but most choose to use a **keg app** to assist in the automatic updating of this file.

Creating an initial `dex.md` is trivial from any modern UNIX shell because the keg directory already contains most of the index information.

```
while read -r readme; do
  id=${readme%/README.md}
  echo "* $(date -r "$readme" -u +%Y%m%d%H%M%S ) [$(head -1 $readme)](/$id)"
done < <(ls -1 */README.md ) | sort -r > dex.md
```

After generating a file in this way it can be updated by hand by simply changing the isosec values and types and titles as needed and resorting the file.
