---
title: 'Image Map: Server-side'
params:
- ismap
---
Deprecated.

Produces HTML image map files. This is a predecessor (circa 1994)
of the IMAP format.  Most servers now use the latter.
[URLs]({{< ref "/docs/attrs/URL.md" >}}) can be attached to the root graph,
nodes and edges. Since edge
links are attached to edge labels, an edge must
have a [label]({{< ref "/docs/attrs/label.md" >}}) for its
URL to be used. For both nodes and edges, if the URL has the escape
sequence `\N` embedded in its string, this will be replaced with the
node or edge name.
