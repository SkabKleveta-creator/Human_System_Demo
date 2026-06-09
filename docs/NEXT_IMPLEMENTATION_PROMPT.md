# NEXT_IMPLEMENTATION_PROMPT.md

## Use This Prompt After Spec Approval

Claude / Opus 4.8

Project: The Human System — P0-A Remember Mara Proof Slice

Task: Implement the approved Minimal Residual Scanner reframe — text/interface only.

Authority, in order:
1. PROJECT_DIRECTION_LOCK.md
2. P0_IMPLANT_REFRAME_NOTE.md
3. HTML_TOUCHPOINT_INSPECTION_REPORT.md
4. MINIMAL_RESIDUAL_SCANNER_PATCH_SPEC.md
5. the_human_system_rpg.html

The Residual Scanner Implant is narrative/diagnostic framing only. It is not a mechanic, battery, upgrade tree, implant tier system, combat, RPG progression, or new resource.

## Approved Changes
1. Add one opening implant-irregularity line in `newState()`:
`['SYSTEM', 'Residual scanner reads outside tolerance. Recalibration advised.']`

2. Reword first-encounter evidence interactions in `buildScenes()` for mug, Tomas' song, and clinic record using the approved spec wording.

3. Reword `evidenceInfo` entries:
- `mug: 'Warm mug — residual heat.'`
- `song: 'Song — residual signal.'`
- `record: 'Record — residual gap.'`

4. Skip optional HUD/status phrase unless clearly safe.

## Hard Constraints
Change only approved touchpoints. No new systems, rooms, combat, upgrade tree, implant tiers, battery, inventory, evidence, characters, endings. Preserve keys, threshold, ending, movement, collision, portals, `collectEvidence()`, `drawDiagnostics()`, `drawEnding()`. Single-file vanilla HTML/JS only.

## Report After Implementation
- BLUF
- Files changed
- Functions changed
- Behavior changed
- Behavior not changed
- Manual test script
- Rollback note

If any requested change would exceed scope, stop and flag it.
