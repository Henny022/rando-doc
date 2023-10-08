# Shuffles
## data lookup
- `VanillaEntrances : data 'areas' by 'name', 'rooms' by 'name', 'entrances' foreach scoped 'name' collect local 'vanilla_exit'`
- `AllChests : data 'areas' by 'name', 'rooms' by 'name', 'chests' collect local 'name'`
- `VanillaChests : data 'areas' by 'name', 'rooms' by 'name', 'chests' foreach local 'name' collect unscoped 'vanilla_contents'`
- `GlobalFlags : data 'global_flags' collect global 'name'`
- `ElementSpots : from data 'areas', 'rooms', 'chests', filter any unscoped 'tags' is "Element Spot" collect unscoped 'name'`
## set spec
## placeholder
`...`
## reverse
`from`
## repeat / repeat individually
- `repeat X : X then repeat X`
- `repeat individually X : take 1 X then repeat individually X`
## map
## connect
## union
## call
## match
