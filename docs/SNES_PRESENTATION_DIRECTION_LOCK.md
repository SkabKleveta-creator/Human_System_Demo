# SNES_PRESENTATION_DIRECTION_LOCK.md

## BLUF
The SNES direction is an SNES-inspired presentation layer over the existing HTML proof slice, not an emulator or hardware rebuild. It splits into two separately approved passes: SNES Shell + Control Map, and SNES In-Game Visual Identity.

## SNES Direction
Single-file vanilla HTML/JS canvas game. The goal is to evoke 16-bit SNES feel through presentation, not hardware emulation, ROMs, controller protocols, libraries, frameworks, or build tooling.

## Two-Pass Structure

### Pass 1 — SNES Shell + Control Map
Move outer chassis from DMG handheld toward wider SNES-controller feel. Add visible X/Y/A/B diamond, preserve D-pad and Select/Start, update labels and footer instructions.

### Pass 2 — SNES In-Game Visual Identity
Richer palette, improved tile rendering, improved sprites, and SNES-style HUD/dialog treatment. Visual only.

Approving one pass does not approve the other.

## Approved Control Map
- D-pad = movement.
- A = confirm / talk / interact / advance dialogue.
- B = cancel / back / close where applicable; existing evidence log behavior.
- X = evidence log / menu-style function using existing `toggleLog()`.
- Y = visible but inert in Pass 1; reserved for future Residual Scan / Inspect.
- Select = display / palette cycle.
- Start = restart for now.

## Y Button Boundary
Y is a real SNES face button, but in Pass 1 it is styled/labeled and bound to no action. It is reserved for a future separately approved Residual Scan / Inspect mapping.

Future Y must not add a scan meter, battery, cooldown, upgrade tier, new evidence detection, hidden-object discovery, or any new evidence system.

## Graphics Boundary
Graphics may improve; gameplay structure may not expand. Better presentation never licenses more game.

## Not Approved
Emulator simulation, merged passes without approval, functional Residual Scan system, changes to `collectEvidence()`, evidence keys, threshold, ending, rooms, portals, combat, upgrade trees, battery, implant tiers, inventory, new evidence, new characters, new story content, Residual Scanner text rewrite, new libraries/frameworks/packages.
