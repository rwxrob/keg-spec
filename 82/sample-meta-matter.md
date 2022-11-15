# Here's a sample of a README.md with meta matter

The first difference is that there is never anything at the beginning of a KEGML file except the title heading. This is by design to keep the content easy to read and grep.

The body of the document here is full of paragraphs and such. But as we come to the end of the file we see a final **raw block** indented four spaces containing YAML with no line returns. This particular example has nothing but `tags` in it. This produces a clean source file that is easy to parse visually and programmatically.

It's worth noting as well that **meta matter** is included in the KEGML document object model (unlike "front matter") so that it is automatically included in the abstract syntax tree (as `meta`) after parsing. A good **keg app** may even parse this simplified structured data as well so that the `meta` node tree appears within the overall document node tree.

    tags: [kegml, sample, metamatter]
