# Simple integer KEG node identifiers

* KEG node identifiers MUST be simple integers beginning at 1.
* KEG node identifiers MUST NOT be reused when content is deleted.
* KEG node titles and content MAY change within a node uniquely identified by an integer.
* KEG node identifiers MUST be included in the [KEGNODES index file](/3).

Numbers are easy to remember, take very little space, and are guaranteed not to break when the title changes. Creating a new node is trivial using this method. For example, here's all that is required on a UNIX system to create and begin editing a new node:

```
cd $KEG
mkdir 2
vi 2/README.md
```

* [Beautiful simplicity of Luhmann's identifiers](/4)
* [Tim Berners-Lee warned against "slugs" in the 90s](/2)