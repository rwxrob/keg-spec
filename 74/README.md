# URL must only appear in footnote, list item, or simple block

* A **URL** MUST ONLY be in **footnote** or **list item** or **URL block**.
* A **keg app** MUST warn if URL use (`://`) is detected **out of spec**.

KEG is strict with regard to clean, consumable **content**. URLs have been a consistent cause of unreadable content both in source and rendered form.[^2] Therefore, URLs in KEGML content are strictly limited to footnotes (usually with a **citation**), list items, and **URL blocks** that begin with a simple field and contain nothing more than the link itself. This is to prevent URLs from ruining source readability as they have done for the Web[^74.1].

[^74.1]: Unfortunately, there is no curing the diseased state of modern Web URLs. Containing them effectively, however, prevents them from infecting KEG content.  
[^2]: Glamour renders *every* inline link by rendering the full URL text immediately after the hyperlinked text.
