# MINIMAL_RESIDUAL_SCANNER_PATCH_SPEC.md

## BLUF
This patch lightly reframes the existing proof slice so the Residual Scanner Implant explains why the player perceives contradiction after Patch 17. It changes no mechanics.

## Patch Objective
The system completed a correction that appears successful; the player's implant is out of tolerance and continues surfacing residue the correction was meant to suppress.

## In Scope
- One opening diagnostic/implant-irregularity line.
- Light rewording of three evidence interactions as residual readings.
- Rewording of evidence log entries.
- Optional static HUD/status phrase only if low-risk.

## Out of Scope
Combat, upgrade trees, battery, implant tiers, inventory, new rooms, new evidence, new endings, new characters, rebellion framing, full RPG progression.

## Proposed Text Changes

### Opening dialog
Add after `The sanctuary has always supported forty-seven residents.` and before `No. Mara was here yesterday.`:

`['SYSTEM', 'Residual scanner reads outside tolerance. Recalibration advised.']`

### Warm mug
- `['SELF', 'The mug is still warm.']`
- `['SELF', 'A ring on the table marks a cup that is gone.']`
- `['SYSTEM', 'That object is unclaimed. It will be processed.']`
- `['EVIDENCE', 'Scanner holds the warmth the record dropped.']`

### Tomas' song
- `['TOMAS', 'Hm hm... hm-hm-hm...']`
- `['SELF', 'Who taught you that song?']`
- `['TOMAS', 'Nobody. I think I have always known it.']`
- `['SYSTEM', 'No resident record contains that melody.']`
- `['EVIDENCE', 'Scanner catches a song with no source.']`

### Blank clinic record
- `['TERMINAL', 'Resident query: MARA.']`
- `['TERMINAL', 'Name: [blank]. Bed: [blank]. Correction timestamp: 02:17.']`
- `['SYSTEM', 'No resident by that name has been assigned here.']`
- `['EVIDENCE', 'The record forgot her, but kept the gap.']`

### Evidence log entries
- `mug: 'Warm mug — residual heat.'`
- `song: 'Song — residual signal.'`
- `record: 'Record — residual gap.'`

### Optional HUD/status phrase
`SCAN: OUT OF TOL` only if it does not crowd `PROOF n/3`.

## Functions Likely Affected
`newState()`, `buildScenes()`, `evidenceInfo`, optional `drawHud()` or `drawWorld()`.

## Behaviors Not Changed
Four rooms, three evidence traces, keys, threshold, `collectEvidence()`, ending, movement, portals, evidence log behavior, palette swap, restart, audio, touch/keyboard controls.

## Risks
Text clipping, tone drift, HUD crowding, scope creep. Mitigation: short text, no new state, no logic edits.

## Approval Gate
No implementation should occur until this patch spec is approved.
