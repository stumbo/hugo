---
defaults: []
flags: []
minimums: []
name: splines
types:
- bool
- string
used_by: G
---
Controls how, and if, edges are represented.

If `splines=true`, edges are drawn as splines routed around nodes; if
`splines=false`, edges are drawn as line segments. If `splines=none` or
`splines=""`, no edges are drawn at all.

(1 March 2007) `splines=line` and `splines=spline` can be
used as synonyms for `splines=false` and `splines=true`, respectively.

In addition, `splines=polyline` specifies that edges should be drawn as
polylines.

(28 Sep 2010) `splines=ortho` specifies edges should be
routed as polylines of axis-aligned segments. Currently, the routing
does not handle ports or, in dot, edge labels.

(25 Sep 2012) `splines=curved` specifies edges should be drawn as curved
arcs.

<TABLE>
<TR>
    <TD><IMG WIDTH="200" VSPACE="10" HSPACE="10" SRC="spline_none.png"></TD>
    <TD><IMG WIDTH="200" VSPACE="10" HSPACE="10" SRC="spline_line.png"></TD>
</TR>
<TR>
    <TD ALIGN="center">splines=none<BR>splines=""</TD>
    <TD ALIGN="center">splines=line<BR>splines=false</TD>
</TR>
<TR>
    <TD><IMG WIDTH="200" VSPACE="10" HSPACE="10" SRC="spline_polyline.png"></TD>
    <TD><IMG WIDTH="200" VSPACE="10" HSPACE="10" SRC="spline_curved.png"></TD>
</TR>
<TR>
    <TD ALIGN="center">splines=polyline</TD>
    <TD ALIGN="center">splines=curved</TD>
</TR>
<TR>
    <TD><IMG WIDTH="200" VSPACE="10" HSPACE="10" SRC="spline_ortho.png"></TD>
    <TD><IMG WIDTH="200" VSPACE="10" HSPACE="10" SRC="spline_spline.png"></TD>
</TR>
<TR>
    <TD ALIGN="center">splines=ortho</TD>
    <TD ALIGN="center">splines=spline<BR>splines=true</TD>
</TR>
</TABLE>

By default, `splines` is unset. How this is interpreted depends on
the layout engine. For `dot`, the default is to draw edges as splines. For all
other layouts, the default is to draw edges as line segments.

Note that for these latter layouts, if `splines="true"`, this
requires non-overlapping nodes (cf. [`overlap`](#d:overlap)).
If `fdp` is used for layout and `splines="compound"`, then the edges are
drawn to avoid clusters as well as nodes.