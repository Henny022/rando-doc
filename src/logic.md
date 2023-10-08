# Logic file format
```
area Foo:
  room Bar:
    node Baz:
      target Blah
      spawn
    Baz -> Baz:
      condition
  room Bar2
  room * +:
    node Extra
  room Bar2 +:
    Extra -> Extra:
      condition
```

From the top, there are a number of scoping contexts.
These are defined globally.
(For tmcr, these are `area` and `room`).

Inside, there are `node`s and `edge`s, defining the overall graph structure.

Nodes are written as `node Name`.
Their children are descriptors, with exports `target`, `self-edge` or `edge-from-beyond-the-void`.
See [exports](yaml.md#export)

Edges are written as `Name1 -> Name2`.
Their children are a number of descriptors with export `edge`, all of which must be satisfied for the edge to propagate reachability.
Two-way edges, written as `Name1 <-> Name2` are syntactic sugar for having an edge with the same conditions both ways.