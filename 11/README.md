# Dynamic nodes

A **dynamic node** is one that requires periodic, programmatic generation. Strictly speaking, dynamic nodes are not officially included in the KEG specification but are worth mentioning due to their usefulness when capturing data that changes over time --- usually automatically.

The idea is simple: put whatever code is required to pull the most recent data into a file named `gen.*` where the suffix is a predictable indicator of the programming language used. That's it. These code files are called **generators**. Suffixes (albeit annoying) are required because the host computer cannot be guaranteed to understand other methods of script interpreter delegation (i.e. she-bang lines).

The following suffixes are recommended:

* `sh` - POSIX shell (ash/dash compatible)
* `bash` - Bash 4.*
* `go` - Go 1.18+
* `perl` - Perl ??
* `rb` - Ruby ??
* `py` - Python 3+

Dependencies on public or private libraries and data is fine, but secrets should never be kept anywhere within a KEG directory or any of its KEG node subdirectories.

The **generator** terminology and technique is well-known to many software developers. For example, the `unicode` package in the Go language does exactly this to pull the actual UNICODE specification and dynamically create code that matches it, albeit infrequently.

By using the **generator** file approach it is trivial to write code that regularly looks for these files and runs them to fetch the latest data at configurable intervals automatically. Or, the generators can be run "by hand" on occasion. And, of course, there is no requirement to keep the generator inside of the node, it just makes management of them easier.

It is also trivial to link to the generator code from the `README.md` file so that the generator source code itself may be included in the node and exposed easily to the reader even after a keg is published to other static forms such as a paper book. This allows the content creator to decide if how and when to expose how that data was obtained.

The inclusion of the `gen.*` generator in the `README.md` file *only* to give insight into the origin of the node content, not to allow anyone following the dynamic node to generate their own. Content creators are under no obligation to include generators that would actually work for anyone but themselves during the local dynamic node generation process. Some creators, however, may elect to make sure that others can generate their own, for example, when *cloning* a dynamic node.

Keep in mind that whatever process executes the generator must also update the [keg dex file](/3) as well. **Followers** will realize that certain nodes are updated more frequently than others and can decide for themselves to ignore specific nodes for that reason (or any reason) if they wish.
