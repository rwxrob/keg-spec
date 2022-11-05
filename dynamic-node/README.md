# Dynamic Node

Dynamic nodes must be periodically generated. The method of generation
must be available to anyone viewing the node. This method is contained
within the `gen.*` file. Dependencies on public or private libraries and
data is fine. The goal is to inform followers of the method in general.

::: Note

The inclusion of the `gen.*` generator is *only* to give insight
into the origin of the node content, not to allow anyone following the
dynamic node to generate their own. Content creators are under no
obligation to include generators that would actually work for anyone
but themselves during the local dynamic node generation process. Some
creators, however, may elect to make sure that others can generate
their own, for example, when *cloning* a dynamic node.

:::

The decision about if and how to communicate the last updated date and
time are completely up to the node content creator, but are usually
included as field within the `DATA.*` file or bit of text in the
`README.md` file.

Whatever process executes the generator MUST update the KEG Directory
`MANIFEST` file as well. Dynamic nodes are marked as "dynamic" ('D')  in
the `MANIFEST` file so that those following can filter out the regularly
updated changes according to their own interests.

Generators MUST be readable files included within the node directory and
begin with `gen` followed by period and suffix indicating the language.
The following suffixes are RECOMMENDED, but not required:

* `sh` - POSIX shell (ash/dash compatible)
* `bash` - Bash 4.*
* `go` - Go 1.18+
* `perl` - Perl ??
* `rb` - Ruby ??
* `py` - Python 3+

Note that suffixes (albeit annoying to some) are required because the
host computer cannot be guaranteed to understand other methods of script
interpreter delegation (i.e. she-bang lines).

Note that generators MUST NEVER be compiled code and MUST NOT contain
secrets of any kind, which will generally be stored in other ways and
pulled in during the generation process.
