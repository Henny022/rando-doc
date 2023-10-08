# Descriptors
## Descriptor Types
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

## Descriptor Rules
### IsEqual
`A = B`
`A ==== B`

### CallDescriptor
run other descriptor
`descriptor arg1 arg2`

### CanAccess
check access to things
`[name arg1 arg2]?`
`[name arg1 arg2]?state`

### AtLeast
Compare County `>=` Constant
`County >= Int`

### Exists
- `∃A - Relation -> value (rule)`
- `∃A <- Relation - value (rule)`
Truthy result
you can use `?` instead of `∃`

### Count
- `+A - Relation -> value (rule)`
- `+A <- Relation - value (rule)`
County result

### Min
`A, B, C`
County elementwise min
Truthy and

### Max
`A; B; C`
County elementwise max
Truthy or

### Statey
- prior `?state`
- post `!state`

### State
`[value1,¬value2]`
you can use `~` instead of `¬`

## Variables
Variable names are prefixed with `v`. They can be either alphanumerical, starting with a capital letter, or arbitrary quoted strings (cannot contain `"` in the name).
Examples:
- `vAlphanum` 
- `v"literally anything"`
