# KEGML Links

KEGML strictly defines different types of links and expressly blocks all
transparent hyperlinking to external content. Links also have specific
semantic meaning and practical use that KEG tools can leverage during
content aggregation and conversion into other publishing formats.

Here's a representative sample of different KEGML link types:

```markdown
Sometimes a reference link to [another node](/another-node) within this
KEG is useful[^note]. Note that such links are never to specific
files and *always* begin with slash.

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

[^note]:
    Bibliographic notes are useful for sources, citations, and other
    traditional bibliographic content that ends up either at the bottom
    of the page as footnotes, or centralized in an appendix depending on
    what form of publication is wanted.

    Note that this stuff has to be indented to work.
```

* [Problems with Web Links](/problems-with-web-links)
* [Node Include Links](/kegml-link-node-include)
* [Node Reference Links](/kegml-link-node-ref)
* [File Include Links](/kegml-link-file-include)
* [Bibliographic Note Links](/kegml-link-note)
* [External Link List Block](/kegml-link-external)
