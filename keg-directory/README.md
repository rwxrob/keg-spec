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

A KEG *directory* MUST contain a `KEG.yaml` file.

* [KEG Directory Schema](/schema-keg)
