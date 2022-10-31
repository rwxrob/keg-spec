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

***Only one heading: the `title`.*** This highly controversial decision is
entirely based on the fact that multiple sections in a KEG Text Node
MUST be replaced by a [importable bulleted
list](importable-bulleted-list) for ease of use from GitHub and Web
sites as well as better, modular organization of the content. This
borrows from the proven Zettelkasten principle of "one best idea" that
can then be composed into other content modularly, not unlike good
software design.

* [Minimal User Information](/minimal-user-information)
