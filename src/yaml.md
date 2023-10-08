# module.yaml spec
```yaml
name: test
version: '1.0'
syntax-version: '0.1'
dependencies:
  - [basicDefinitions, ">= 1.0, < 2.0"]
soft-dependency: []
provides:
  descriptors:
    test:
      arguments:
      - scoped
      stateful: false
      type: truthy
      export: edge-from-beyond-the-void
  logic-sugar:
    entrance:
      type: multi
      expands-to:
        - warp
    "|":
      type: operator
      replacement: or
  descriptor-definitions: []
  logic:
    - "logic/*.logic"
  patches: []
  shuffles: []
  data: []
```

## version numbers
Version numbers use SemVer, aka. `major.minor.patch`.
Dependency versions allow `*` for any version or `>=` and `<` for specifying ranges.
Ranges can be left open by leaving out a bound.

## dependencies
Dependencies are other modules, providing e.g. descriptor declarations used in this module.  
Soft dependencies are modules with which compatibility is asserted, ensuring this module is loaded after any soft dependencies.

## Descriptor Declarations
Descriptors may be used by other descriptors, or in the logic.

### Export
For using them in the logic, the export property determines how they may be used:

| Export | Description |
|---------|---------|
| none | Cannot be used in logic. The default value |
| edge | Applied to an edge, evaluated to propagate reachability |
| target | Applied to a node, doesn't evaluate and instead may be tested for reachability in descriptor definitions |
| edge-from-beyond-the-void | Applied to a node, evalued to give reachability (pretends there is an edge from a reachable node outside the logic graph) |
| self-edge | Applied to a node, pretends there is an edge from the node to itself with it. Useful for manipulating state (TODO) |

### State
State is not yet implemented.

### Type
Type determines the type of the evaluation of the descriptor. Only truthy descriptors can be used in logic.

### Arguments
A descriptor can take any number of [thingies](descriptors.md#thingies) as arguments, any of which may be scoped or unscoped.

### Consuming

Not yet implemented. Will be used for key logic and kinstones.

## Syntactic sugar

Sugar to be applied to the logic file before evaluation.  
Two variants: Multi and Operator.

### Multi
Allows one to write one descriptor as a shorthand for a set of descriptors in logic. The number and scoping of arguments should be identical in all replacements, but other properties (like export) needn't agree.

### Operator

Infix operators for logic.

## remaining files
`descriptor-definitions`, `logic`, `patches`, `shuffles` and `data` list remaining files in the module.
These paths may contain wildcards (`*`).
