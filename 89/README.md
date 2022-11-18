# Leave indexing up to apps and developers

* This **specification** MUST specify how the **keg index file** is updated.
* This specification MUST NOT specify how other indexing[^89] is to be accomplished.
* A **KEG app** MAY provide indexing on any number of fields.
* A keg app MAY create and manage any files within a **keg** except those that are reserved.
* A keg app MUST handle reserved files as specified.
* A keg app SHOULD consider not adding unnecessarily large files.

Those creating **keg apps** will want to create keyword indexes, category and tag lists, word counts, and other reference content that is dynamically generated and updated upon every keg node update. Approaches and needs will widely vary depending on the content and purpose. Therefore, only the following minimal list of files is reserved for KEG use:

* `keg`
* `meta`
* `README.md`
* `{1-9}+`

This leaves plenty of room for any directory or file other than these available for use in the root **keg directory** including `index.html` for **keg apps** that plan to render and push to the **KEG Web**.

[^89]: For a time, formalizing the inclusion of text-based indexes was entertained. But the work of dealing with indexing has to be assigned to either a consumption tool or a generator. The method and type of indexing will also vary greatly depending on the content and needs of the content consumers, therefore decided to omit any specification of how to index KEG content other than the **keg index file** since it is so crucial to a standardized exchange of KEG content.
