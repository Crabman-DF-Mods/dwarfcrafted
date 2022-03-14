# Changelog
This file will document changes to this project.

Unfortunately, [Semantic Versioning](https://semver.org/) is not compatible with Dwarf Fortress raw mods because most changes would be `MAJOR` save incompatible changes, so this project uses a custom versioning convention instead; for a given version number `MAJOR.MINOR.PATCH`, increment the:
- `MAJOR` version for a large overhaul of many existing objects, or the addition of a new class of features/objects that were previously impossible. This would usually correspond with new major DF releases, and therefore is likely not compatible with existing saves, or even previous DF versions.
- `MINOR` version for new objects being added or large changes to existing objects; likely not save compatible.
- `PATCH` version for bug fixes, _small_ edits to objects, code cleanups, or documentation changes. Almost always compatible with previous saves.

The "Unreleased" heading is for changes that are in the repo but not in any published version (they are probably not ready yet).

The meaning of each subcategory of change is as follows:
- Added: A new file, section in a file, or object was created, or a feature added to an object. If a creature ID exists but is unimplemented/has `[DOES_NOT_EXIST]` and cannot be spawned even in the testing arena, this doesn't count as being added.
- Changed: An existing file or object/property has been edited/changed. Changes that will not be recorded include most code comments inside files, updates to `CHANGELOG.md` that are simply recording other changes, or `README.md` updating the mod version or promoting something from "planned content" to "content".
- Removed: An object, property, or section of a non-raw file was deleted.
- Fixed: A bug/error or a typo was fixed. If it's a fix, it will not be recorded under any of the above headings.

## [Unreleased]

### Added
- Hyper rabbits; a hyperactive species of rabbit with long whiskers, messy fur, and an unusual color scheme
- Magma cows; cows made of magma, found deep underground
- Bone Spiders; gigantic spiders with a layer of bone protecting them
- Giant azaleas; huge azaleas that grow as large as an oak tree
- Glow lichen; a glowing underground fungus
- Netherrack, which is magma-safe and soft like clay, but can be fired in a kiln into the more solid "netherware". It doesn't generate anywhere as a stone, but titans and the like can be made of it
- Nether quartz, which is just a valuable white quartz. It doesn't generate anywhere yet, but titans and the like can be made of it
- Glowstone. Just like the other Nether materials, it doesn't generate anywhere yet, but titans and such can be made of it

### Changed
- Updated the ingame descriptions of all creepers; they mention the fact that they explode now
- Wardens and shriekers now heal their bone tissues 20x faster (which is now 2x as fast as normal creatures skin heals)
- Prismarine is no longer a normal sedimentary ocean layer stone; it now generates in extremely rare single chunks
- Prismarine is now 8 times more valuable than regular stones

### Removed
- Removed dark oak trees from the planned feature list because they apparently exist in real life; Quercus velutina, the eastern black oak
- Removed blackstone from planned feature list because it apparently has close enough real-life counterparts that I can use instead
- Removed nether gold ore from planned feature list because I figure the existing "native gold" will probably be sufficient when the time comes to add the nether and have gold ore in netherrack

### Fixed
- Typos in `README.md`
- Changed code indentation from spaces to tabs in a few places

## [v1.1.0] - 2022-02-22

### Added
- Prismarine soliders; large, ancient statues with tentacled faces, created to protect undersea temples which appear not to exist anymore
- Prismarine colossuses; huge megabeasts much like the prismarine soliders, but far, far bigger
- Creeders; horrid abominations that take the explosiveness of creepers, and add arachnophobia
- More details in the readme file about the mod content

### Changed
- Made the readme file more up to date; the DF RAW LS is out of alpha, and "Creature Variants" is better phrasing for the planned content than "Misc Creatures"
- Made the readme file more readable and expanded the planned content list slightly
- Made male enderdragons drop eggs when they die, not just females

### Fixed
- Made creepers move a bit faster, because 1 kph max speed was kind of stupid and just a placeholder I forgot to change; now it's 3 kph crawling, 6 kph walking

## [v1.0.1] - 2021-12-31
### Fixed
- Fixed ravagers and stalkers blood being described as "nothing blood"
- Fixed the mooshroom, cluckshroom and moolip variants; all of them were broken except mooblooms, the red mooshrooms, and red cluckshrooms, oops!

## [v1.0.0] - 2021-12-20
### Added
- `CHANGELOG.md` file for a changelog, woo!
- Details in `README.md` about the planned and current magic types
- Added 4 creatures, and more moo/cluckshroom variants to the planned content list in `README.md`
- Iceologer, evoker, and mage castes for illagers
- Brown, plump helmet, dimple cup, tower-cap, and fungiwood variants of mooshrooms
- Mooblooms and moolips
- Cluckshrooms, in all the same variants as mooshrooms
- Shriekers
- Furnace golems
- Snow golems
- Melon golems
- Copper golems
- Added furnace, snow, melon and copper golems to villager civs
- Sculk veins (a kind of deep cavern plant)
- Creepers now have "creeper juice" blood
- Slimes and tropical slimes bodies changed; now includes 3 sensory organs
- Gave magma cubes 2 eyes
- Gave iron golems an extra prefstring ("long arms")
- Gave allays the ability to open doors

### Changed
- Edited initial description in the `README.md` to include the acronyms of the games
- Shulkers now functional as much as DF allows pretty much, though they still don't spawn
- Creeper fever's "fever" symptom is now resistable
- Slimes and tropical slimes descriptions and tissue coloring updated
- Updated mooshrooms description
- Mooshrooms mushroom tissue now heals
- Mooshrooms mushroom tissue now uses a plural for a more evocative description
- Merged mooshrooms `SET_TL_GROUP` for their hair and mushroom tissues, since the color should always be the same
- Sculk tissue on wardens now heals
- Renamed magma cube "magma cream" tissue to "magma cream core", and changed the tissue ID accordingly (`CORE` instead of `MAGMA_CREAM`)
- Magma cubes now drop magma cream as a liquid, not a solid rock
- Updated illagers description, unique from testificates
- Made allays count as "natural"
- Made `MC_ECTOPLASM_TEMPLATE` (allays body material) immune to cold damage
- Increased the heat damage point for `MC_ECTOPLASM_TEMPLATE` to 10508 urists/914.4°C (same as ignite point)

### Removed
- Removed iron golems `EXTRAVISION`, so they need their eyes now
- Removed magma cubes `EXTRAVISION` since they have eyes now
- Removed ears and toes from iron golems

### Fixed
- Fixed magma cubes "magma cream" tissue using the wrong material
- Fixed magma cubes "crust" tissue being `FUNCTIONAL`, which made them die if it was damaged
- Fixed illager skin color being described like "her upper lip's skin is X" instead of just "her skin is X"
- Typo in phantoms alert sound ("hungry screech", when it should have been "hungrily screech")

## [v0.1.1] - 2021-12-13
### Changed
- Formatted `LICENSE` file to be more readable
- Added sculk to planned plants list in `README.md`
- Replaced endermite mouth with mandibles
- Made creeper biome `FOREST_TAIGA` instead of `TAIGA`

### Fixed
- Removed `MUSCULAR_ONLY` from guardians electricic shock "unconsciousness" symptom
- Fixed empty `SPATIAL_SENSE` arg for endermen
- Fixed broken attacks for endermite and silverfish
- Fixed villager civs so that they can have iron golems
- Fixed some syndromes creature targeting (see ghasts and endermites)
- Fixed ghast fireballs
- Fixed ghast baby names (had no plural, so it was invalid)
- Fixed Wildfire helmet materials/tissues
- Fixed allay memory memory attribute (had too many args)
- Fixed glares `LOW_LIGHT_VISION` (had a higher value than allowed)

## [v0.1.0] - 2021-12-12
The initial public release. It contains the following:
- Villager, illager and piglin entities/civs
- Creepers
- Testificates
- Piglins
- Ravagers
- Allays
- Phantoms
- Silverfish
- Slimes
- Mooshrooms
- Wardens
- Guardians and Elder Guardians
- Glow Squids
- Iron Golems
- Endermen
- Endermites
- Enderdragons
- Withers
- Wither Skeletons
- Ghasts
- Magma Cubes
- Blazes
- Striders
- Hoglins
- Barnacles
- Chompers
- Wildfires
- Glares
- Tropical Slimes
- Stalkers
- Prismarine
- Partially implemented shulkers

<!--Links-->
[Unreleased]: https://github.com/Crabman-DF-Mods/dwarfcrafted/compare/v1.1.0...HEAD
[v1.1.0]: https://github.com/Crabman-DF-Mods/dwarfcrafted/compare/v1.0.1...v1.1.0
[v1.0.1]: https://github.com/Crabman-DF-Mods/dwarfcrafted/compare/v1.0.0...v1.0.1
[v1.0.0]: https://github.com/Crabman-DF-Mods/dwarfcrafted/compare/v0.1.1...v1.0.0
[v0.1.1]: https://github.com/Crabman-DF-Mods/dwarfcrafted/compare/v0.1.0...v0.1.1
[v0.1.0]: https://github.com/Crabman-DF-Mods/dwarfcrafted/releases/tag/v0.1.0