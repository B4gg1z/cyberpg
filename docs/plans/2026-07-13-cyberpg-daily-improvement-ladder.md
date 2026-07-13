# CyberPG Daily Improvement Ladder

> **For Hermes:** Use `cyberpg-one-room-pass` for small safe daily work, but follow this ladder so the project moves forward in the right order instead of drifting into random polish.

**Goal:** Make daily CyberPG updates stack into a stronger one-room SPD-style slice with better tactical decisions, cleaner run texture, and clearer future architecture.

**Architecture:** Keep the prototype browser-first and single-file for now, but treat each pass as part of a larger ladder: tactical truthfulness first, then player decision density, then encounter variety, then reward/progression texture, then content packaging. Avoid spending full passes on decorative polish unless it improves readable tactics.

**Tech Stack:** Vanilla HTML, CSS, JavaScript in `index.html`, plus `README.md`, `VERSION`, and plan docs in `docs/plans/`.

---

## Current baseline (v0.1.17)
- One authored room with key → chest → Volt Fang → clear room → exit arc
- Click-again route commitment
- On-board enemy intent badges with damage callouts
- Objective pulse marker
- Last-seen enemy ghost memory
- Legacy reward persistence between runs
- Stronger preview text for attack odds and first-step route danger

## Daily-pass rules
1. **Read first**
   - `README.md`
   - `docs/plans/2026-07-10-cyberpg-reboot-one-room.md`
   - this ladder file
2. **Pick one bounded gameplay-forward change**
   - Prefer decision quality, tactical truthfulness, or room arc over cosmetics.
3. **Ship the whole truth**
   - If mechanics change, update HUD text, preview text, overlay copy, README, and visible version string together.
4. **Verify live every time**
   - Load in browser
   - Check console for JS errors
   - Run a browser-console proof for the new state/interaction
   - Run `node --check` on extracted script
5. **Keep the release resumable**
   - Update `README.md` current status and `VERSION`
   - Add one line to this plan if the ladder priority changed

---

## Priority ladder for upcoming passes

### Ladder 1: Player decision density
**Why first:** The room already reads better. Next gains should make the player choose better, not just see better.

**High-value pass shapes:**
- Manual heal-flask inventory/use instead of auto-resolve pickup
- Stronger wait / hold-position tradeoffs
- Safer vs greedier chest timing incentives
- Route previews that call out what you give up, not only what hits you

**Files:**
- Modify: `index.html`
- Update: `README.md`, `VERSION`

**Verification ideas:**
- Prove item pickup changes underlying state instead of only copy
- Prove the new choice consumes a turn when appropriate
- Prove HUD and preview lines agree before/after use

### Ladder 2: Enemy role separation
**Why next:** The room gets more interesting when enemies force different answers, not just bigger numbers.

**High-value pass shapes:**
- Distinct hunter pressure behavior
- Cleaner guard lunge telegraph / punish window
- Seer beam counterplay improvement
- One new enemy role only if the current room still fits cleanly

**Verification ideas:**
- Force exact enemy states in browser console
- Confirm board badges, intent panel, and actual outcome agree

### Ladder 3: Reward / progression texture
**Why after that:** Once the room decisions are sharper, run-to-run reward choice matters more.

**High-value pass shapes:**
- Better legacy descriptions and immediate run impact clarity
- Reward choices that change route incentives
- Stronger distinction between survivability / aggression / utility boons

**Verification ideas:**
- Choose a legacy, reset, verify stored state and live hero stats/items

### Ladder 4: Encounter arc escalation
**Why later:** Escalation is worth more after the core choices are good.

**High-value pass shapes:**
- Chest alarm pressure that changes pathing
- Exit unlock drama and clearer cleanup state
- Small reinforcement timing beats

### Ladder 5: Architecture boundary prep
**Why last for now:** Only spend a full pass here if micro-passes start fighting the single-file setup.

**High-value pass shapes:**
- Data extraction for rewards/enemies/map content
- Cleaner state helpers that reduce future breakage
- README / plan / release-note hygiene for interruption-safe continuation

---

## Good daily-pass templates

### Template A: Tactical truth pass
1. Reproduce one misleading or under-informative state
2. Fix mechanics and presentation together
3. Verify both browser visuals and underlying JS state
4. Bump version

### Template B: Decision pass
1. Find a spot where the game auto-resolves a choice for the player
2. Convert it into an explicit tactical decision
3. Add a clear control / HUD affordance
4. Verify cost, benefit, and state transitions live

### Template C: Room-arc pass
1. Improve one phase of the room beat
2. Make the objective/status text reflect the new phase cleanly
3. Verify before, during, and after states in the browser

---

## Red flags — do not spend a full pass on these alone
- purely prettier gradients
- flavor-copy-only updates
- invisible cleanup with no player-facing gain
- adding a new mechanic without preview/HUD truthfulness
- adding a new reward without proving persistence next run

---

## Next recommended pass
**Manual heal flask inventory + explicit use control.**

Reason:
- It upgrades the RPG side immediately
- It creates a real tactical choice instead of automatic healing
- It pairs nicely with the existing `Smuggled Tonic` legacy
- It is meaningful without needing a second room or major architecture split
