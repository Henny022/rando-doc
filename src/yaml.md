# module.yaml spec
```yaml
name: test
version: '1.0'
dependencies: []
softdependency: []
provides:
  descriptors:
    test:
      arguments:
      - scoped
      stateful: true
      type: truthy
  descriptor-definitions: []
  logic: []
  patches: []
  shuffles: []
  data: []
```

## version numbers
Version numbers use SemVer, aka. `major.minor.patch`.
Dependency versions allow `*` for any version or `>=` and `<` for specifying ranges.
Ranges can be left open by leaving out a bound.
## Descriptor Definitions
[Descriptors](Descriptors)
## logic
[logic file spec](LogicFiles)
## Shuffles
[Shuffles](Shuffles)
## Data
[Data](Data.md)
