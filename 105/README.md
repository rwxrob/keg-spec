# Quote block limitations

* A **quote block** MUST only contain a **paragraph**.
* A **quote block** MUST NOT contain multiple lines.

KEGML respects the limitations of most literary quotations that would appear at the beginning of articles or chapters requiring that quote blocks consist only of a single line or paragraph.

Markdown allows quote blocks to include entire Markdown documents and sub-documents.[^105] KEGML supports this as well but requires such content be contained in a **div block** instead. Div blocks are much easier to manage given their clear starting and ending markers. Div blocks also do not require every line begin with a right angle bracket (`>`) as Markdown does.

[^105]: Originally, this was to meet the needs of email thread quoting which was common at the time of Markdown's invention.
