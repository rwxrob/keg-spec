# Isosec

An **isosec** is the UTC current time in ISO8601 (RFC3339) with a T to separate out the time and a Z to indicate UTC (ex: 20060102T030405Z). This time-based unique identifier is preferred over others since it can easily be determined with nothing more than a watch or wall clock with a second hand and parses correctly with numeric and lexical sort tools. It also loads very nicely into any database engine.

