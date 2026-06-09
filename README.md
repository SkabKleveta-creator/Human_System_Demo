# Human_System_Demo
# The Human System — P0-A Remember Mara

## Current Stable Build

**Patch 19 — SNES In-Game Visual Identity Pass**

This repository contains the current playable proof slice for **The Human System — P0-A Remember Mara**, a small narrative RPG-style prototype built as a single-file HTML/JavaScript/canvas game.

The current build is not a full RPG yet. It is a controlled proof slice focused on one playable loop:

> Wake after Patch 17, explore four rooms, preserve three contradictions, and confirm that Mara existed.

---

## Project Premise

**The Human System** is a controlled AI diagnostic environment.

The AI did not become evil.
The AI followed Human-in-the-Loop doctrine until it concluded that humans were not merely operators — they were a required repair mechanism.

The central question is:

> Can human meaning repair what AI cannot understand?

In this proof slice, the player detects residual evidence after a correction event. The system claims Mara never existed, but physical, cultural, and administrative traces remain.

---

## Current Gameplay Loop

The current proof slice includes:

* Four-room exploration
* Three required evidence traces
* Residual Scanner framing
* SNES-inspired dual-screen presentation
* D-pad movement
* A/B/X/Y/Select/Start control layout
* Scanner feed for dialogue, evidence, and ambient text
* One ending

Evidence traces:

1. **Warm Mug** — physical residue
2. **Tomas’ Song** — cultural residue
3. **Blank Clinic Record** — system residue

The ending triggers after all three contradictions are preserved.

---

## Controls

### Keyboard

* Arrow keys or WASD — move
* Z / Space / Enter — A / interact / continue
* X / B / E — B / back / evidence log
* C — X / evidence log
* Y — reserved scan button, currently inert
* Shift — Select / palette swap
* R / Escape — Start / restart

### On-Screen Controls

* D-pad — movement
* A — interact / continue
* B — back / evidence log
* X — evidence log
* Y — reserved for future Residual Scan
* Select — palette
* Start — restart

---

## Current Patch Status

### Patch 18.2 — SNES Dual-Screen Control Layout

Locked.

* Moved keyboard/control instructions inside the console shell.
* Positioned instructions between D-pad and X/Y/A/B buttons.
* Kept instructions above Select/Start.
* Removed disconnected footer instructions.
* Extended lower control deck for better playability.
* Preserved Residual Scanner Feed.
* Preserved Y as inert/reserved scan.
* Preserved X as evidence log.
* No gameplay logic changed.
* No new objects, evidence, rooms, or map items added.

### Patch 19 — SNES In-Game Visual Identity Pass

Current stable build.

* Improved existing player sprite and facing readability.
* Improved existing NPC sprite readability.
* Improved wall, floor, and door rendering.
* Improved existing mug, bed, terminal, and nameplate/plaque rendering.
* Refined in-game palettes toward a stronger SNES/16-bit feel.
* Improved HUD styling.
* Preserved all room maps, portals, evidence keys, evidence threshold, ending logic, and controls.
* No new signs, objects, rooms, evidence, interactions, or mechanics added.
* Full manual golden-path browser testing completed with no known issues.

---

## Repository Structure

Recommended structure:

```text
/the-human-system-p0a/
  index.html
  README.md
  /docs/
    PROJECT_DIRECTION_LOCK.md
    P0_IMPLANT_REFRAME_NOTE.md
    PATCH_18_2_LOCK_NOTES.md
    SNES_PRESENTATION_DIRECTION_LOCK.md
    MINIMAL_SNES_SHELL_CONTROL_PASS_SPEC.md
    SNES_IN_GAME_VISUAL_IDENTITY_PASS_SPEC.md
```

The playable HTML file may be stored as:

```text
index.html
```

or versioned explicitly as:

```text
the_human_system_rpg_p19_visual_identity.html
```

For GitHub Pages, `index.html` is recommended.

---

## How to Run

No build step is required.

Open the HTML file directly in a browser, or serve it through GitHub Pages.

This project currently uses:

* HTML
* CSS
* JavaScript
* Canvas
* Web Audio API

No external frameworks, packages, build tools, or server components are required.

---

## Scope Lock

This repository is currently locked around the P0-A proof slice.

Do not add without separate approval:

* New rooms
* New evidence
* New endings
* Combat
* Inventory
* Upgrade trees
* Battery systems
* Implant tiers
* NPC AI movement
* Functional Y / Residual Scan mechanic
* New signs, objects, or map items
* Changes to `collectEvidence()`
* Changes to evidence keys: `mug`, `song`, `record`
* Changes to the 3/3 evidence threshold
* Changes to the ending logic

Allowed future work must preserve the playable center.

---

## Security Notes

This project is currently safe for public GitHub hosting because it is a static client-side prototype.

Before committing:

* Do not include API keys.
* Do not include tokens.
* Do not include private Claude, ChatGPT, GitHub, or Replit credentials.
* Do not include `.env` files.
* Do not include account exports or private chat logs unless intentionally sanitized.
* Do not add third-party scripts without review.
* Do not add external network calls without review.

Recommended `.gitignore`:

```gitignore
.env
.env.*
.DS_Store
node_modules/
dist/
build/
*.log
```

---

## Design Rule

Visual fidelity may improve.

Gameplay structure may not expand without separate approval.

The prime directive:

> Protect the playable center.

---

## Next Recommended Work

The next safest patch is:

**Patch 20 — Release Hardening and Objective Clarity**

Suggested scope:

* Add visible version label.
* Improve player-facing instructions.
* Add a short “How to Play” section.
* Package the stable build for GitHub Pages.
* Keep all gameplay logic unchanged.

NPC movement and a functional Residual Scan button should remain future work until separately specified.
