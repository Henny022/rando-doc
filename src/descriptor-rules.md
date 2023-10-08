# Descriptor Rules

A rule is written as `head: body.`

For any descriptor, you can define any number of rules.
The maximum/or of all rules is the resulting value of the descriptor.

## Rule Head

The head of a rule is the descriptor's name followed by its arguments.
These can be variables, which will be bound at the call-site, or constants, in which case the rule will only apply to invocations with that value (pattern-matching).

## Rule Body

The body of a rule is built from the following constructions:

### IsEqual
- `A = B`
- `A == B`

### CallDescriptor
run other descriptor
- `descriptor arg1 arg2`

### CanAccess
check access to things
- `[name arg1 arg2]`
- `[name arg1 arg2]?state`
  see [State](#state)

### AtLeast
Compare County `>=` Constant
- `County >= Int`
- `County >= inf`

### Exists
- `∃vA - Shuffle -> value (rule)`
- `∃vA <- Shuffle - value (rule)`

Truthy result: Is there an A shuffled to/from the given value satisfying `rule`?

You can use `?` instead of `∃`

### Count
- `+vA - Shuffle -> value (rule)`
- `+vA <- Shuffle - value (rule)`

County result: How many As shuffled to/from the given value satisfy `rule`.

### Min
`A, B, C`

County elementwise min
Truthy and

### Max
`A; B; C`

County elementwise max
Truthy or

### Statey
Not yet implemented
- prior `?state`
- post `!state`

#### State
Not yet implemented
- `[thingy1,¬thingy2]`

you can use `~` instead of `¬`