# Descriptors

## Thingies

The arguments and variables in descriptors are thingies.
[Shuffles](shuffles.md) associate thingies to one another.

Thingies can be scoped (e.g. `MinishWoods.Main.West`) or unscoped (e.g. `Sword`).

## Variables
Variable names are prefixed with `v`.
They can be either alphanumerical, starting with a capital letter, or arbitrary quoted strings (cannot contain `"` in the name).
Examples:
- `vAlphanum` 
- `v"literally anything"`

## Descriptor Types

Evaluating a descriptor gives a value (not a thingy).
Any descriptor has a type, determining what values it will evaluate to.

Values can be stateful (not yet implemented) and/or depend on the usage of consumables (not yet implemented, e.g. keys).

### Truthy
values:
- `true`, `⊤`
- `ool`
- `false`, `⊥`

Implicitly casts to County

### County
values:
- `0`, `⊥`
- positive integers (decimal)
- `inf`, `∞`, `⊤`

You can add `+` and multiply `*` Countys

### State

Not yet implemented.

### Consuming

Not yet implemented.
