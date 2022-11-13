# KEGML link restrictions

```pegn
Name        <- FileName / NodeName
RootLink    <- '/' Name
ParentLink  <- '../' Name
LocalLink   <- Name
```

A KEGML link within a **node** `README.md` file MUST NOT point to anything outside of the **keg** to which it belongs.

A **relative link** MUST NOT point to anything more than one level of depth distance from the file containing it.

Therefore, a link MUST be one of three types: root, parent, local.

A **root link** MUST begin with a slash.

A **parent link** MUST begin with two dots and a slash.

A **local link** MUST NOT have any prefix (unlike HTML and Markdown).

Local includes both files and other node directories underneath.
