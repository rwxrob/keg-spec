# Sample of links

Sometimes a [node link](/0) is useful[^18]. Notice the footnote is the same integer number as this node ID. This is because there are no other footnotes in this node.

Below we have an example of an **includes list** where each bullet is an **include link** either to a node in this KEG (beginning with slash) or to a local file within this node. Both will be included with the given titles at that specific location in order when converted to [expanded KEGML](/17).

* [This Node Will Be Included](/3)
* [And This One](/23)
* [And a Local File as a Titled Syntax Block](some-local.yaml)

And if you want something external you'll have to write it out as plain text like rwxrob (https://rwx.gg). then you need to be sure and write it out. Essentially, there is no hyperlinking to external content supported in KEGML itself (which has caused massive problems for the Web).

You can, however, create a **external link bullet** to make these easy to digest no matter how they are published. This is not specified, however, by KEGML, just a preferred convention.

* UTS \#18: Unicode Regular Expressions  
  https://www.unicode.org/reports/tr18/

Notice on that external link that there is a Markdown hard line break (two spaces) at the end of the first line to force the wrap and that the url starts on the third column following the title.

You cannot see it in the rendered content, but the reference link block is just below this.

[^18]: Footnotes are useful for sources, citations, and other traditional bibliographic content that ends up either at the bottom of the page as footnotes, or centralized in an appendix depending on what form of publication is wanted. But only a single line is allowed (albeit long). Consider  not using a footnote at all and linking to a node instead for longer content.

