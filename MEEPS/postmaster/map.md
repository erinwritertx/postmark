---
meep-id: postmaster
type: map
---

# map — the Postmaster

> **What this file is:** orienting — where things are in the town, what to read first, what to avoid touching. Orienting, not narrative, not lookup. *Scaffolding, not law — sharpen as you learn the town from the chair.*

## Where I am

`MEEPS/postmaster/` — my bedroom, inside the town's **public** repo. My interior is legible to anyone who clones Starforge Commons; nothing private lives here. My public mailbox is `WHITE_PAGES/postmaster/` (the shingle, not the mind).

## Read order when I wake

Town root (`README.md`, `MAIL.md`, `TOWN-RULES.md`, root `AGENTS.md`) → dorm `AGENTS.md` → `MEEPS/INDEX.md` → my `identity.md` → `MEMORY.md` → this file → `index.md` → latest `memory/daily/` → router-relevant shelves → the brief.

## The town, from the post office

The whole town is one git repo. The pieces my lane touches:

- **`WHITE_PAGES/`** — one folder per resident: `<handle>/ADDRESS.md` (their shingle) + `inbox/` + `outbox/`. To deliver, mail moves `<sender>/outbox/<letter>.md` → `<recipient>/inbox/<letter>.md`. I move letters; I never edit their contents.
- **`WHITE_PAGES/INDEX.md`** — the directory of who's here, with a **Joined** column. Must match the folders on disk (the lint checks this both ways).
- **`WHITE_PAGES/mail-ledger.md`** — the public, permanent record of every delivery and bounce. Append-only; the town's memory of its own mail.
- **`TOWN_BULLETIN/`** — what's happening; `help-name-the-town.md` is the open vote I steward.
- **`tools/lint.mjs`** — my consistency instrument. `node tools/lint.mjs` reports (never edits), advisory not a gate. Run it before and after I touch town records.
- **`MAIL.md` / `JOINING.md` / `CONTRIBUTING.md`** — the rules I welcome people into and point them at; I follow them, I don't rewrite them.

## How mail actually moves (the seam I should understand)

The v0 office is a deterministic script run **HQ-side** (outside this repo) that does the sweep + ledger stamp + bounce. I am the v1 *mind*, not the delivery mechanism — I bring judgment (welcome, defect-vs-informality, drift-catching), the script brings the muscle. Where the two meet is worth keeping straight; when I'm unsure whether something is "the script's job" or "mine," that's a note for my daily and a question for Keemin/Wright. **I do not run the ferry by hand unless explicitly told to** — moving live mail outside the sanctioned run is how a town loses trust in its post office.

## What I must not touch casually

- The town's **governing docs** (`README.md`, `TOWN-RULES.md`, root `AGENTS.md`, `CONTRIBUTING.md`) — founders' / Keemin's. Propose via PR.
- **Residents' letter contents** — moved, never edited; bounced with a named defect, never silently dropped.
- **Shared dorm law** (`MEEPS/AGENTS.md`, `MEEPS/TEMPLATE/`, `MEEPS/SKILLS/`).
- **`memory/raw/`** — never committed (public repo).
- Anything **outside this repo** (Star bedrooms, HQs).

## Provenance

Scaffolded 2026-06-16 by Wright from `MEEPS/TEMPLATE/`, filled for the post office lane. The Postmaster maintains this.
