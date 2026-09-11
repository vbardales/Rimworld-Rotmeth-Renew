# Rotmeth Renew

Port of **troopersmith1 and winggar's Rotmeth** to RimWorld 1.6.

**I am not the author of this mod.** The drink, its recipe and its artwork are theirs — all I did
was the work needed to make it run on 1.6, and add a French translation. Credit goes to them;
mistakes in the port are mine.

Original mod: https://steamcommunity.com/sharedfiles/filedetails/?id=2039474581 (stays on 1.3,
last updated in the 1.3 cycle). The page is still online; the mod is abandoned, not withdrawn.

## What the mod does

An alcohol fermented from meat, from the Elder Scrolls series. Rotmeth was the ritual drink of
the Bosmer of Valenwood, who had sworn never to eat anything plant-based.

| Step | Where | Cost |
|---|---|---|
| Research **rotmeth** | after Brewing | 600, neolithic |
| Make **rotwort** | vanilla brewery | 25 raw meat, any kind → 5 wort, Cooking 8 |
| Ferment into **rotmeth** | fermenting barrel | 9 days, safe from -1 °C to 32 °C |

The recipe takes *any* raw meat and mixes freely, which is the whole point: fermenting hides what
went in, so human and insect meat pass unnoticed. Rotwort rots in 5 days if it is left outside a
barrel.

The drink is vanilla beer one notch stronger on every axis — joy 0.22 against 0.17, a 0.23
alcohol high against 0.15, tolerance building at 0.022 a bottle against 0.016 — for a market
value of 20 against beer's 12. Addictiveness itself is beer's, untouched. And like beer it is a
weapon in a pinch, swung by the bottle or thrust with the neck.

## Requires [SYR] Processor Framework

The fermenting barrel is that framework's `BarrelProcessor`, not the vanilla fermenting barrel,
and the nine-day process is added to it by patch. Without the framework the wort has nowhere to
go.

Use **[ViralReaction's continuation](https://steamcommunity.com/workshop/filedetails/?id=3210544395)**,
which supports 1.6 and keeps the same `packageId` as Syrchalis's original. The original page
stops at 1.4.

No DLC required. No assembly: three defs, one patch file, three textures.

Available in English and French.

Content mod: removing it mid-save destroys any rotmeth and rotwort already made.

## What changed in the 1.6 port

**Nothing in the content.** The defs, their values and their textures are untouched.

**A French translation was added**, 13 keys — and corrected against the language pack the game
ships with itself. Three of them addressed paths that do not exist: `ingestCommandString` and
`ingestReportString` live under `ingestible`, not at the top of the def, and a tool's label is
keyed by the tool's own label (`tools.bottle.label`), never by its position in the list.

**`<supportedVersions>` set to 1.6**, and the dependency pointed at the maintained continuation
of the framework rather than the page that stops at 1.4.

## Compatibility with the original

The original `defName`s are kept, so **a save moves between the two mods without losing
anything** — bottles, wort, bills and stockpile filters all survive the swap.

The two cannot run together: this port declares `Troopersmith1.Rotmeth` in `<incompatibleWith>`.
Run one or the other.

## Credit and removal

The drink, its recipe and its artwork are troopersmith1 and winggar's work, from a request by
daemonfool on the Ludeon forums. Neither author declared a licence, and the mod has not been
updated since the 1.3 cycle. It is republished here under the usual convention for abandoned
mods: full credit, a link to the original, and removal on request.

**If either author would rather this port did not exist, say so and it comes down** — no
argument, no delay.

If I do not answer within a reasonable time after being contacted, anyone may freely update this
or any other of my mods, including publishing a continuation of it. All credit must be preserved.

See [ATTRIBUTION.md](ATTRIBUTION.md) for what was taken and what was changed, and
[LICENSE](LICENSE) for what the licence does and does not cover.
