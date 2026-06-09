# RESIDUAL_SCANNER_MANUAL_TEST_SCRIPT.md

## BLUF
Validates that the Residual Scanner reframe changes only text/interface presentation while preserving the proof-slice loop.

## Test Environment
Browser/manual play only. Desktop keyboard and touch/pointer both checked. No automated harness required.

## Pre-Test Checks
- Game loads.
- Boot overlay appears.
- Tap/click starts game.
- No `SCRIPT ERROR` or `ERR` overlay.
- Controls respond.

## Golden Path Test
1. Start game.
2. Clear opening dialog; confirm implant-irregularity line displays and does not clip.
3. Move through all four rooms.
4. Inspect warm mug; confirm evidence registers.
5. Inspect Tomas; confirm evidence registers.
6. Inspect clinic record; confirm evidence registers.
7. Confirm HUD reaches `PROOF 3/3`.
8. Confirm ending triggers: `MARA EXISTED`.
9. Restart; confirm fresh wake state and evidence reset to 0/3.
10. Open evidence log; confirm revised entries render without clipping.

## Regression Checks
Movement, collision, portals, evidence collection once per item, repeat inspection lines, ending threshold, palette swap, restart, touch controls, keyboard controls.

## Failure Conditions
Script error, missing/clipped opening line, evidence fails to register, count exceeds 3, ending fires early or fails, evidence can be collected twice, restart fails, text hides meaning, or any new system appears.

## Pass Criteria
All pre-tests, golden path, and regression checks pass with no failure conditions. Only observable differences are approved text/interface changes.
