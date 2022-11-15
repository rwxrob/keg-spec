# KEGML element: inflect span

* An **inflect span** MUST indicate voice or tone inflection.
* An **inflect span** MUST ONLY appear within a **paragraph block** or **list item**.
* An *inflect span* starts with a single star (`*`) followed by non-space.
* An *inflect span* ends with single star (`*`) preceded by non-space.

An **inflect span** is identical in meaning and purpose to the [HTML5 `i` element](/23) indicating a "change in tone or voice" only. Italics is usually be used to visually indicate this change in tone but is certainly not required.

Note that within a **footnote** the same markup syntax for **inflect** takes on a different semantic meaning depending on the bibliographic style being used by the content creator. For example, the following footnote uses this markup for APA style guidelines:

```kegml
[^23.1]: "HTML Living Standard - 4.5.20 The b element" (2022, November 10). *WHATWG*. https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-i-element
```

Note that `*WHATWG*` corresponds to italic text per APA style. In the case of APA, italic font face provides a semantic distinction as well as a predictable visual style.
