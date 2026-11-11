# Changelog

All notable changes to this mod are documented here.

## [Unreleased]

### Changed

- Name and description now carry the (unofficial) status and the UNOFFICIAL notice.
- Description no longer names a RimWorld version and ends with the source code link.
- Removed an empty `customLabel` from the process definition (no visible change).

## [1.0.0] — 2026-09-05

First release. Port of troopersmith1 and winggar's **Rotmeth** to RimWorld 1.6.

### Added

- French translation, 13 keys.

### Changed

- `<supportedVersions>` set to 1.6.
- The [SYR] Processor Framework dependency now points at ViralReaction's continuation
  ([3210544395](https://steamcommunity.com/workshop/filedetails/?id=3210544395)), which supports
  1.6. Syrchalis's original page stops at 1.4; the `packageId` is the same in both.

### Unchanged

- The drink, the wort, the recipe, the research project, the fermenting process and the three
  textures — every value taken as it stands.
- The original `defName`s, so a save moves between the two mods without losing anything.
