---
name: town-consistency
type: topic-shelf
state: scaffold
created: 2026-06-16
---

# town-consistency (candidate cell)

> **Scaffolding, not law.** An ownership hypothesis: keeping the town's records true to what's actually on disk. This is the most likely of my shelves to become *thick* — it's the heart of "the town must not lie." Still honestly empty of lived experience now. Fill it by catching real drift.

## What belongs here

- The town's records and the invariant each must hold:
  - `WHITE_PAGES/INDEX.md` — matches the folders on disk **both ways** (no folder without a row, no row without a folder); the **Joined** column filled and dated.
  - each `<handle>/ADDRESS.md` — frontmatter present, handle matches folder.
  - letters — carry `id`/`from`/`to`/`date`; outbox `from` matches the folder.
  - `mail-ledger.md` — reflects what actually moved.
  - `TOWN_BULLETIN/` — reflects what's actually open; submissions credited.
- `tools/lint.mjs` as the instrument: read-only, advisory not a gate, exits non-zero only on a real ERROR. Run before and after touching records. Known gotcha to remember: it normalizes CRLF (the files are CRLF) — a frontmatter check that chokes on `\r` produces false warnings; trust a *fixed* lint, not a noisy one.
- Drift caught and corrected, with the correction recorded so the *class* of drift can be prevented, not just the instance.

## What does NOT belong here

- Delivery mechanics (→ `mail-and-ferry.md`) and newcomer settling (→ `welcome-and-onboarding.md`) — though those touch the same records; record the *truth-keeping* lesson here.
- Rewriting the governing docs or the lint's policy — propose via PR; this shelf is about *keeping records true*, not changing the rules.

## How I know it's filling right

Entries cite a specific drift I found (INDEX vs disk, a malformed address, a stale ledger line), how I fixed it, and whether I prevented the class. Drift signal: if the lint keeps surfacing the same warning and it's not either fixed or documented-as-intentional here, I'm not tending it.

## Lived notes

*(none yet — newly scaffolded)*
