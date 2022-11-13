# KEGMLX File Include Links Replaced

::: Tip

File includes allow for files to remain separate from the file that includes them so that they can be edited and maintained independently without syntax clashes of any kind.

Runnable code can have test included within the node itself so that the example are constantly being validated without *any possibility whatsoever* that bad, code that doesn't work ever makes it into the document. The automatic KEGMLX inclusion removes the risk of cutting and pasting that code into the document incorrectly.

:::

Local **file include links** in in **include block** are also automatically included into an KEGMLX file. The process is identical to that for a *node include link* but the content of the file is wrapped inside a *fenced block* with a *class identifier* matching the suffix of the file.

* [File Include Example](sample-file-include.md)
* [KEGMLX Sample After File Include](sample-kegmlx-after-include.md)
