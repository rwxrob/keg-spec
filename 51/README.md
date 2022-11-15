# No Markdown reference links (except footnotes)

* A **KEGML document** MUST NOT contain Markdown reference links.

The following is not allowed in KEGML:

```md

Here is a [reference link] within a paragraph.

[reference link]: /some-thing
```

Regular markdown allows for reference links the targets of which are in a separate block later in the document. These make reading Markdown source much easier when extremely long URLs are allowed as link targets (such as with [the Web](/2)). With KEGML, however, such links are not needed since all inline link targets are extremely short.

