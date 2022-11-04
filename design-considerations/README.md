# Design Considerations

* **Soft returns cause viewing and `diff` problems**

A soft return is a single line return in the middle of a paragraph block. In Markdown such are handled the same as an extra space and ignored. However, this practice has always been controversial.

For instance, lines that have the exact same words on them will be reported by `diff` and other tools just for reformatting.

Content creators can also never agree on what the optimal column width should be: 80, 72, 108? This creates huge frustration because one wrap column width looks great for someone while another one looks horrible.

Better to let the content creator and consume decide *their* preferred column width so that they can view it on the most things without a problem. This is in line with Gruber's "source should be as readable as the render" principle. Whether a reader has minimized a TMUX pane to 10x10 in a corner or filled the screen, the automatic wrapping will remain as readable as possible.

* **Use of 4-letter suffix for YAML**

The YAML creators prefer 4 letters over three (`.yml`).

* **Never any "front matter"**

Front matter has always been a bad idea since it violates fundamental principles of separation of concerns confusing content creators and software applications alike.

* **Leave cache indexing up to tools**

For a time formalizing the inclusion of text-based indexes was entertained. But work of dealing with indexing has to be assigned to either a consumption tool or a generator. The method and type of indexing will also obviously vary greatly depending on the content and needs of the content consumers, it was therefore decided to omit any specification of how to index KEG content other than the [KEGNODES file](/kegnodes-file) since it is so crucial to a standardized exchange
of KEG content.

It is expected that those creating KEG tools will want to create keyword indexes, category and tag lists, word counts, and other reference content that is dynamically generated and updated upon every KEG node update. The KEGNODES manifest is crucial to this since it eliminates the need to re-index the entire KEG on every update, only those nodes that have risen to the top of the KEGNODES file because of updates since the
last pull of the file.

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
