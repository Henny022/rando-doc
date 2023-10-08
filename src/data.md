# Data
## data definition
- `Elements : {"EarthElement", "FireElement", "WaterElement", "WindElement"}`
## data combination
- `VanillaEntrances : data 'areas' by 'name', 'rooms' by 'name', 'entrances' foreach scoped 'name' collect local 'vanilla_exit'`
- `AllChests : data 'areas' by 'name', 'rooms' by 'name', 'chests' collect local 'name'`
- `VanillaChests : data 'areas' by 'name', 'rooms' by 'name', 'chests' foreach local 'name' collect unscoped 'vanilla_contents'`
- `GlobalFlags : data 'global_flags' collect global 'name'`
- `ElementSpots : from data 'areas', 'rooms', 'chests', filter any unscoped 'tags' is "Element Spot" collect unscoped 'name'`
