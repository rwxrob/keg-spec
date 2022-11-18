# Rune

* A **rune** MUST be defined as any valid Unicode codepoint.

A rune is another term for "Unicode codepoint" which is "any value in the Unicode codespace; that is, the range of integers from 0 to 10FFFF."[^100.1]

Runes are different than "characters" (or "chars") since a rune is not limited in size to one byte. A rune varies in size from one to 4 bytes in length. In the Go programming language a rune is an alias for a 32 bit integer (`int32`).[^100.2]

[^100.1]: "Glossary of Unicode Terms" (2022). http://unicode.org/glossary/#code_point
[^100.2]: Pike, Rob. "Strings, bytes, runes and characters in Go" (2013, October 23). *The Go Blog*. https://go.dev/blog/strings
