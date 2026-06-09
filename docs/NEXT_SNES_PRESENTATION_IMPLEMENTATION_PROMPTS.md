# NEXT_SNES_PRESENTATION_IMPLEMENTATION_PROMPTS.md

## Prompt 1 — Implement SNES Shell + Control Map Pass

Paste after MINIMAL_SNES_SHELL_CONTROL_PASS_SPEC.md is approved.

Claude / Opus 4.8

Project: The Human System — P0-A Remember Mara Proof Slice

Task: Implement the approved SNES Shell + Control Map Pass — presentation/control only.

Authority, in order:
1. PROJECT_DIRECTION_LOCK.md
2. P0_IMPLANT_REFRAME_NOTE.md
3. SNES_PRESENTATION_DIRECTION_LOCK.md
4. MINIMAL_SNES_SHELL_CONTROL_PASS_SPEC.md
5. the_human_system_rpg.html

Implement ONLY the approved shell/control pass:
- Restyle outer chassis toward a wider SNES-controller silhouette.
- Replace diagonal A/B cluster with X/Y/A/B diamond: Y left, X top, B bottom, A right.
- Add `.btn-x` / `.btn-y` styling and new button elements.
- Preserve D-pad and Select/Start behavior.
- Map A = `interact()`, B = `toggleLog()`, X = `toggleLog()`, Select = `changePalette()`, Start = `newState()`.
- Y is INERT: styled and labeled, bound to no action. Reserve it for future Residual Scan.
- Update labels and footer instructions.

Hard constraints: presentation/control-map only; no functional Y; no scan system; no new mechanics, rooms, evidence, endings, combat, upgrade trees, battery, implant tiers, or inventory; no changes to `collectEvidence()`, keys, threshold, ending, rooms, portals, Residual Scanner text, or canvas/mobile behavior. Single-file vanilla HTML/JS only.

Manual test: game loads; no error; D-pad moves; A interacts; B log; X log; Y does nothing; Select cycles palette; Start restarts; golden path reaches 3/3 and “MARA EXISTED”; touch and keyboard work; tap sizes adequate; canvas not cropped.

Rollback: replace with pristine pre-pass copy.

## Prompt 2 — Implement SNES In-Game Visual Identity Pass

Paste after SNES_IN_GAME_VISUAL_IDENTITY_PASS_SPEC.md is separately approved.

Claude / Opus 4.8

Project: The Human System — P0-A Remember Mara Proof Slice

Task: Implement the approved SNES In-Game Visual Identity Pass — visual rendering only.

Authority, in order:
1. PROJECT_DIRECTION_LOCK.md
2. P0_IMPLANT_REFRAME_NOTE.md
3. SNES_PRESENTATION_DIRECTION_LOCK.md
4. SNES_IN_GAME_VISUAL_IDENTITY_PASS_SPEC.md
5. the_human_system_rpg.html

Implement ONLY the approved visual identity pass:
- Refine `PALETTES` toward richer 16-bit color while keeping keys compatible.
- Improve `drawTile()`, `drawPerson()`, `drawObject()` rendering.
- Improve `drawHud()` and dialog/log box treatment in `drawWorld()`.
- Optionally refine screen CSS overlays.

Hard constraints: visual rendering only; no gameplay changes; no map/collision changes; no new tiles that change collision; no new mechanics, evidence, interactions, endings; no changes to `collectEvidence()`, movement, update loop, portals, threshold, ending, or Residual Scanner text; preserve canvas and HUD readout; single-file vanilla HTML/JS only.

Manual test: game loads; no error; all rooms render; walls/doors read correctly; sprites/objects legible; HUD/dialog readable; golden path reaches ending; controls/mobile unchanged.

Rollback: replace with pristine pre-pass copy.
