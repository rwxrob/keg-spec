# KEG User Schema

The KEG User schema (also contained in `KEG.yaml`) extends the KEG
schema for personal KEGs associated with a specific user. Such KEGs
contain uniquely identifying information about the user required for
content attribution as well as an optional `FOLLOW` and `AVOID` list
files that promote community policing of KEG content based on trust
between users.

User KEGs also optionally contain the cached copies of other user KEGs
(in `/cached`). Usually, these map directly to those in the `FOLLOW`
list, but not always since tools are allowed --- and encouraged --- to
only cache specific KEG nodes rather than entire KEGS where possible.

Users control their own `/cached` copies, their update intervals, and
personal, localized search preferences.

The KEG `/cached` also provides some level of KEG backup redundancy as
multiple users follow the same KEGs creating their own individual cached
copies. This communal `/cached` KEG memory has its own implications that
all KEG users should understand before participating in KEG as a creator
or consumer.

* [YAML Schema](DATA.yaml)
* [JSON Schema (from YAML)](DATA.json)
* [FOLLOW File](/follow-file)
* [AVOID File](/avoid-file)
