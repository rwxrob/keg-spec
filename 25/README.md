# File include link

* The **link target** of a **file include link** MUST be a **file**.
* The **file** must be in same directory as `README.md` containing link.
* The **link text** MUST be a valid **title**.
* A **keg app** MUST examine **link text** for exclamation point prefixes.
* **Expanded** MUST replace link content of target file.
* **Expanded** MUST create heading from link text unless exclamation point.
* **Expanded** MUST enclose target file as-is if double exclamation point.
* **Expanded** MUST enclose target file content in 10-tick fenced block if no exclamation point.
* **Fenced** block MUST have **class identifier** set to file suffix (if any).

::: Tip

File includes allow for files to remain separate from the file that includes them so that they can be edited and maintained independently without syntax clashes of any kind.

Runnable code can have test included within the node itself so that the example are constantly being validated without *any possibility whatsoever* that bad, code that doesn't work ever makes it into the document. The automatic KEGMLX inclusion removes the risk of cutting and pasting that code into the document incorrectly.

:::

* [File Include Example](sample-file-include.md)
* [KEGMLX Sample After File Include](sample-kegmlx-after-include.md)
