# Secondary Nodes

Secondary nodes are those that are not
[included](/kegml-link-node-include) anywhere within the KEG. Secondary
nodes are therefore assumed to have content that is secondary to the
included content.

Aggregation tools handle this secondary content in whatever way seems
best for the tool and final output, perhaps into an appendix or section
of its own so that links to it elsewhere in the KEG will resolve to
them. Secondary nodes MUST be included, however. Their semantic
importance is too great to simply ignore (unlike [orphan
nodes](/orphan-nodes) that are often excluded entirely from
aggregation)

Secondary nodes MUST also have semantic priority over [bibliographic
notes](/kegml-link-note) even though they are very similar in purpose.
In fact, often a bibliographic note will grow large enough to warrant
its own secondary or included node instead.
