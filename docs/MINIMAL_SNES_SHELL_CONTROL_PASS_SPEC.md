# MINIMAL_SNES_SHELL_CONTROL_PASS_SPEC.md

## BLUF
Smallest approved SNES shell/control pass: restyle outer chassis toward SNES-controller feel, replace diagonal A/B cluster with X/Y/A/B diamond, preserve D-pad and Select/Start, update labels and footer instructions. X routes to existing evidence log; Y is inert/future-reserved. Specification only.

## Objective
Move outer presentation from DMG handheld to SNES-inspired controller without adding gameplay systems.

## In Scope
- CSS/HTML shell layout changes.
- X/Y/A/B diamond: Y left, X top, B bottom, A right.
- Preserve D-pad behavior.
- Preserve Select/Start behavior.
- X = evidence log/menu using existing `toggleLog()`.
- Y = inert visual button reserved for future Residual Scan / Inspect.
- Updated labels and footer keyboard instructions.

## Out of Scope
New mechanics, scan system, evidence, rooms, endings, combat, upgrade tree, battery, implant tiers, inventory, Residual Scanner text rewrite.

## Required Touchpoints
- HTML face-button markup in `.main-controls` / `.ab-buttons-wrapper`.
- CSS shell layout: `.console-wrapper`, `.console-body`.
- CSS diamond: `.action-btn`, `.btn-a`, `.btn-b`, new `.btn-x`, `.btn-y`.
- `KEY_BINDINGS`: add X carefully; Y only if needed for inert press feedback.
- `handleInstantInputs()`: add X case calling `toggleLog()`; do not add functional Y case.
- `triggerButtonFeedback()`: add `.btn-x`; `.btn-y` only if key feedback is desired.
- `attachPointerControls()`: likely no change; confirm `[data-key]` behavior.
- Footer keyboard instructions.

## Button Behavior Proposal
- A keeps `interact()`.
- B keeps `toggleLog()` / close log.
- X routes to `toggleLog()`.
- Y is inert; do not call `interact()` and do not create scan behavior.
- Select keeps `changePalette()`.
- Start keeps `newState()`.

## Risks
Layout on small screens, touch target crowding, keyboard binding collisions, X/B duplicate-log clarity, scope drift toward making Y useful too soon.

## Approval Gate
No implementation should occur until this shell/control spec is approved.
