Sometimes a reference link to [another node] within this KEG or [file] within this node is useful[^note].

Below we have an example of an **includes block** where each bullet is a link either to a node in this KEG (beginning with slash) or to a local file within this node. Both will be included with the given titles at that specific location in order when converted to [expanded KEGML].

* [This Node Will Be Included](/include-me)
* [And This One](/include-me-too)
* [And a Local File as a Titled Syntax Block](some-local.yaml)

And if you want something [external](/kegml-link-external) then you need
to be sure and write it out. Essentially, there is no hyperlinking to
external content supported in KEGML itself (which has caused massive
problems for the Web). An external link in KEGML, therefore, simply a
list item formatted in a particular way.

* UTS \#18: Unicode Regular Expressions  
  https://www.unicode.org/reports/tr18/

Notice on that external link that there is a Markdown hard line break
(two spaces) at the end of the first line to force the wrap and that the
url starts on the third column following the title.

You cannot see it in the rendered content, but the reference link block is just below this.

[another node]: /another-node
[expanded-kegml]: /kegml-expanded
[file]: somefile.whatever
[^note]: Bibliographic notes are useful for sources, citations, and other traditional bibliographic content that ends up either at the bottom of the page as footnotes, or centralized in an appendix depending on what form of publication is wanted. But only a single line is allowed (albeit long). Consider linking to a node instead for longer content.

