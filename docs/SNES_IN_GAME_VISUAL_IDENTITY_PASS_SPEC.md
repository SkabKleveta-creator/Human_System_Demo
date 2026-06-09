# SNES_IN_GAME_VISUAL_IDENTITY_PASS_SPEC.md

## BLUF
Later separately approved pass that restyles the in-game canvas from DMG dot-matrix toward SNES-inspired 16-bit RPG visual language while preserving gameplay logic. Visual only.

## Objective
Improve in-game presentation while preserving the 160×144 canvas, four rooms, three evidence traces, movement, portals, 3/3 threshold, single ending, and Residual Scanner text.

## In Scope
Palette refinement, tile rendering improvements, character sprite improvements, object sprite improvements, HUD/dialog visual treatment, screen/bezel CSS if relevant.

## Out of Scope
Room map changes, new tiles that change collision, new mechanics, new evidence, new interactions, new endings, changes to `collectEvidence()`, movement, portals, or Residual Scanner text.

## Likely Touchpoints
`PALETTES`, `drawTile()`, `drawPerson()`, `drawObject()`, `drawHud()`, `drawWorld()`, dialogue box rendering, and screen CSS.

## Preservation Rules
Rooms/maps unchanged; tile characters keep collision meaning; evidence keys and threshold unchanged; `collectEvidence()` untouched; movement/update loop untouched; portals/spawns unchanged; ending unchanged; Residual Scanner text unchanged; canvas dimensions unchanged; palette swap, restart, audio, touch and keyboard controls unchanged.

## Risks
Readability, mobile viewport, contrast, sprite clarity, accidental collision/logic drift. Rendering and collision must remain separated.

## Approval Gate
No implementation should occur until this visual identity spec is separately approved.
