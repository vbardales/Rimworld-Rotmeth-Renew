# Rotmeth — attribution

A 1.6 port of **Rotmeth**, by **troopersmith1** and **winggar**
([2039474581](https://steamcommunity.com/sharedfiles/filedetails/?id=2039474581)), itself born of
a request by **daemonfool** on the Ludeon forums.

## Status: public

The source mod is **dead** — it declares 1.1 to 1.3 and nothing further — and **no licence is
declared anywhere**, checked in the mod's files, in its `About.xml` and on its Steam page.
Republished with credit by name and a removal clause.

## What changed in the port

**Nothing.** The defs are taken as they stand: the drink, the wort, the recipe, the research and
the `ProcessDef`. Only a French translation was added.

## The dependency nearly disqualified it

Rotmeth requires **[SYR] Processor Framework** — its wort ferments for nine days in the
`BarrelProcessor`, and its patch adds a process to that building's comp.

The framework's original page
([2633514537](https://steamcommunity.com/sharedfiles/filedetails/?id=2633514537)) **stops at
1.4**, which led me to conclude the port was impossible without porting the framework first. That
was wrong: the continuation by ViralReaction
([3210544395](https://steamcommunity.com/workshop/filedetails/?id=3210544395)) goes up to
**1.6**, **keeps the same `packageId`**, and was already installed.

**The sign to follow:** several mods declaring this framework as a dependency — Booze-O-Matic,
Vandar's composter — advertise 1.6. *A mod does not declare a dead dependency while supporting
the current version.*

The check was redone **inside the framework's `1.6/` folder**, not only at its root:
`BarrelProcessor` and `ProcessorFramework.CompProperties_Processor` exist unchanged, and the
`ProcessDef` fields this mod sets are all present on the framework's own `Beer` example. Both
patches apply.

Like Vanilla-like Wheat, that framework is itself a republication of an abandoned mod, with
`<author>Syrchalis</author>` preserved and no licence file. It is the precedent this publication
rests on.

## What was taken

`Rotmeth` (the drink), `Rotwort` (the wort), `Make_Rotwort` (at the vanilla brewery), the
`Rotmeth` research project and the `ProcessorFramework.ProcessDef` of the same name — three def
types carrying the same name, which is legal, each def database being separate.

The original `defName`s are kept, and the source mod is declared in `<incompatibleWith>`.

## Notes from the port

- The mod ships **no assembly**: three defs, one patch file and three textures.
- The drink's textures follow the vanilla `Graphic_StackCount` layout — a folder named after the
  `texPath`, holding `Rotmeth_a.png` and `Rotmeth_b.png`. Two variants rather than vanilla beer's
  three; the collection graphic handles any count.
- The French injection was corrected against the language pack the game ships with itself. Three
  keys addressed paths that do not exist: `ingestCommandString` and `ingestReportString` live
  under `ingestible`, and tool labels are keyed by the tool's own label, never by its index.
  Vanilla beer, which this drink copies field for field, spells all four out.
- `Troopersmith1.Rotmeth` in `<incompatibleWith>` is the expected form of the original
  `packageId`, and it could not be verified on the files: the source mod is no longer installed
  and its Workshop page is dead. The author half is evidenced — troopersmith1's other published
  mod, Death Rattle Continued, declares `Troopersmith1.DeathRattle` — so the naming scheme is
  `Troopersmith1.<ModName>`. The mod-name half is inference. Casing does not matter either way:
  RimWorld compares on `packageIdLowerCase` and keeps the original only for display. A wrong
  value here is inert — it disables nothing — but it also guards nothing.
