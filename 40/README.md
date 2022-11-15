# Footnote

* A **footnote** MUST consist of a **footnote marker span** within a **paragraph** or **list item** and a **footnote paragraph** within a **footnotes** block linked to the marker by a common **footnote ID**.
* A **footnote ID** MUST begin with same integer of current node ID.
* A **footnote ID** MAY omit rest of reference if only footnote in node.
* A **footnote ID** MUST add dot (`.`) and incremental int if more than one footnote.
* A **keg app** MUST warn when migrating or importing nodes with footnotes.

A KEGML **footnote** works exactly as they do in Pandoc Markdown except that the text used in the **footnote ID** must be unique across the entire keg scope. Therefore, use of an integer identifier that matches that same file containing the footnote is required. For multiple footnotes a dot and incremental integer are additionally required.

```kegml
This is a sentence with a footnote.[^1.1]
```

Using this approach to footnotes makes creating an **optional index** of all footnotes trivial since all footnote references are guaranteed to be unique within a given keg.

::: Warning

Migrating or importing a node usually involves changing the node ID, which will also require the update to all footnote IDs in that node. Any **keg app** supporting such functionality must, therefore, warn about the footnote IDs and optionally correct them as well. This is one reason for such specificity in format of a footnote ID. (Pandoc allows references to be about anything.)

:::
