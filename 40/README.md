# Footnote

* A **footnote** MUST consist of a **footnote marker span** within a **paragraph** or **list item** and a **footnote paragraph** within a **footnotes** block linked to the marker by a common **footnote ID**.
* A **footnote ID** MUST be unique to the content node
* A **keg app** MUST qualify the footnotes relative to their content node IDs

A KEGML **footnote** works exactly as they do in other markdown variations except that each footnote reference (normally near the bottom of the content node) must be in its own block to avoid confusion and increase readability.[^3] They also may not contain multiple lines. Such things should be put into their own content node instead.

[^3]: Many markdown renderers (such as Glamour) will consider a block of multiple footnote references as just another paragraph. Therefore, in order to ensure consistency, each footnote reference must be in its own block (surrounded by blank lines).

```kegml
This is a sentence with a footnote.[^1.1]
```

Using this approach to footnotes makes creating an **optional index** of all footnotes trivial since all footnote references are guaranteed to be unique within a given keg.

::: Warning

Migrating or importing a node usually involves changing the node ID, which will also require the update to all footnote IDs in that node. Any **keg app** supporting such functionality must, therefore, warn about the footnote IDs and optionally correct them as well. This is one reason for such specificity in format of a footnote ID. (Pandoc allows references to be about anything.)

:::
