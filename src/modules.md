# Modules

To enable self-contained modifications of the game in a re-usable manner, the definitions to make the randomizer work are split into modules.

Typically, these would center around a set of patches and the description of these patches to make the randomizer shuffle things correctly in the presence of the contained changes.
Some notable exceptions to that rule would be a module describing the base game, or providing common descriptors to avoid needing to repeat things.

## Examples
- vanilla game
- keysanity
- keasy
- homewarp
- glitch patches
- glitched logic
- intro skip
- open fusion
- progressive items
- entrance rando

## What can modules do
- change item pool
- change logic
- add patches
- add/change shuffle instructions
- add descriptors
- change game data

## module files

A module is self-contained in a folder.
At the top level is a file named `module.yaml` that describes the module.
- [module.yaml spec](yaml.md)
- [Descriptor definitions](descriptors.md)
- [Logic](logic.md)
- [Patches](patches.md)
- [Shuffles](shuffles.md)
- [Data](data.md)
