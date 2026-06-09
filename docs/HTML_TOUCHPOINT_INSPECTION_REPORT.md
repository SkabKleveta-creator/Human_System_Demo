# HTML_TOUCHPOINT_INSPECTION_REPORT.md

## BLUF
The minimal Residual Scanner reframe can be added with low-risk text/interface edits only. No mechanic, state field, loop, data structure, or control binding needs to change.

## Confirmed Touchpoints

### `newState()` — required, low risk
Adds one opening dialog line establishing implant irregularity. Must not change `evidence: new Set()`, `pendingEnd`, `diagnostics`, scene/player fields, or the meaning of the existing wake lines.

### `evidenceInfo` — optional, low risk
Three-entry log-text map keyed `mug`, `song`, `record`. Values may be reworded, but keys must not change. Log renderer truncates to 27 characters.

### `buildScenes()` — optional, medium risk
Contains the three `collectEvidence(...)` dialogue arrays. May reword the first-encounter evidence text. Must not change rooms, maps, portals, spawn coordinates, object IDs/kinds/blocks/coordinates, or talk callback structure.

### Three `collectEvidence()` calls — optional, medium risk
Text surface for mug, song, and record residual-reading wording. Must preserve call signature, IDs, and first/repeat array shape.

### `collectEvidence()` — excluded, high risk if edited
This is the loop mechanic. Do not touch. Preserve Set dedupe, evidence sound, `size >= 3` threshold, pending ending behavior, and return contract.

### `drawHud()` — optional, medium risk
Possible static status phrase. Must not remove scene name or `PROOF n/3`. No counter/resource/status system.

### `drawWorld()` — optional, low risk
Possible prompt wording. Must preserve control-hint accuracy, dialogue/log render structure, and wrap limits.

### `drawDiagnostics()` — excluded, high risk if repurposed
Error-only overlay. Do not couple implant flavor to the error path.

### `drawEnding()` — excluded
Do not touch for the minimal reframe. Preserve “MARA EXISTED” and one-ending structure.

## Required for Minimal Reframe
- Add one `newState()` opening dialog line establishing scanner irregularity.

## Optional Later
- Reword `evidenceInfo` entries.
- Reword three first-encounter evidence dialogue arrays.
- Add one static HUD/prompt phrase if layout-safe.

## Not Approved
New implant state, charge, tier, level, battery, new evidence, new rooms, new objects, changed ending, changed threshold, or any change to `collectEvidence()`.

## Preservation Rules
Four rooms, three evidence traces, evidence keys, evidence threshold, one ending, movement, portals, evidence log behavior, no new systems.

## Risk Assessment
Risks are cosmetic/tonal: text clipping, tone drift, HUD crowding, and temptation to misuse diagnostics as implant status.

## Recommended Next Action
Draft/approve the minimal Residual Scanner patch spec before implementation.
