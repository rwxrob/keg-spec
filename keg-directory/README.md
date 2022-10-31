# KEG Directory

A *KEG directory* (also referred to as a "keg site" or just "keg") MUST
contain one or more [KEG nodes](/keg-node), each with a uniquely
identifying directory name within the KEG directory itself.

Any unique identifier type is allowed but the following types are
RECOMMENDED since any human can easily create them:

* slug - title predictably converted
* isosec - node title is uncoupled from name

While slugs are easier to navigate, they can create problems when
interlinking is allowed or encouraged. If the title changes, so must the
slug. This has long been a problem with Web content organization.

A KEG *directory* itself fulfills the requirements for a KEG *node*
except for the obvious exception that it MUST contain other nodes (where
normally a *node* may not).

A KEG *directory* MUST contain a `KEG.yaml` file in addition to the 

## ISO Second ("isosec")

An *isosec* is the GMT current time in ISO8601 (RFC3339) without any
punctuation or the T. This unique identifier is preferred over others
since it can easily be determined with nothing more than a watch or wall
clock with a second hand.

## KEG Markup Language (KEGML)

KEGML is a simplified (and deliberately limited) version of Pandoc
Markdown with standardized extensions for Math notation (MathJax)
fenced, semantic divisions, tables, and bibliographic references. It is
suitable for conversion into most rich publications formats including
academic papers, books, novels, articles, and blog posts.

Although tables are supported, it is strongly RECOMMENDED that *data
nodes* be used instead where possible since the data is immediately
usable in such form. Content creators may opt to use a generator for the
tables in their `README.md` files and store the actual data in the
`DATA.*` file instead. It is also RECOMMENDED to limit tables to one per
*text node*.

**Images MUST NOT be included in KEGML.** Unlike most other flavors
of Markdown, KEGML deliberately omits images of any kind. This is
because all images MUST be contained within their own *figure nodes*.
This promotes the use of images to convey something that cannot
otherwise be described with text. Such a limitation promotes the widest
possible range of participants and eliminates superfluous decoration
which bloats content and complicates the publishing process.

## Dynamic Node

Dynamic nodes must be periodically generated. The method of generation
must be available to anyone viewing the node. This method is contained
within the `gen.*` file. Dependencies on public or private libraries and
data is fine. The goal is to inform followers of the method in general.

:::note
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

* [KEG Schema](/schema-keg)
