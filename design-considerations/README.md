# Design Considerations

**Use of 4-letter suffix for YAML**  

The YAML creators prefer 4 letters over three (`.yml`).

**Never any "front matter"**  

Front matter has always been a bad idea since it violates fundamental
principles of separation of concerns confusing content creators and
software applications alike.

**YAML as structured data format**  

YAML has become the world-wide standard for human-friendly structured
data. Any communication or configuration between any KEG tooling MUST
use simplified YAML (which includes JSON). This limitation does not
apply to [DATA nodes](/data-node), which allow all major forms of
structured data.

***Use HTML5 rationalization for `italic` and `bold`*** instead of
"emphasis" and "strong emphasis".

***SLUG-from-title conversion algorithm*** is irrelevant since it is up to
the content creator to create it by creating the name of the directory.
This obliterates the problems of incompatible slug-from-title conversion
algorithms (Pandoc, GitHub, Vue, etc.)

**Single title heading only**

Linking to headings has always been problematic in HTML and Markdown. No
one can agree on an automated way to convert a title to a local anchor
link URL, for example. The proposed addition of CommonMark attributes
promises to address much of this

KEG addresses the problem at a higher level, by forcing the knowledge
into a graph data structure. This allows tools to come up with their own
methods of aggregating, outlining, and linking to the content depending
on the tool and final target output.

This idea about knowledge content organization is not new or unique. In
fact, it borrows heavily from "mind map" applications and designs
originating from the proven Zettelkasten principle of "one best idea"
that can then be composed into other content modularly, not unlike good
software design. It's the simplest and most sensible solution to the
problem of organic content creation.

* [Minimal User Information](/minimal-user-information)