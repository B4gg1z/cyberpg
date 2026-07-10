# CyberPG reboot one-room plan

> For Hermes: keep this reboot browser-first and prove the feel with one room before any larger architecture.

**Goal:** Ship a one-room Shattered Pixel Dungeon-inspired prototype that is actually playable and worth testing.

**Architecture:** Single-file browser prototype first. HTML/CSS/JS with an authored room, turn loop, fog-of-war, enemy turns, pickup chain, and readable combat log.

**Tech stack:** Vanilla HTML, CSS, JavaScript.

## Scope for v0.1.1
1. One authored room
2. Grid movement
3. Turn-based enemy movement with pathfinding
4. Bump-to-attack combat
5. Limited visibility + explored memory
6. One key -> one chest -> exit unlock room beat
7. One ranged enemy to create line-of-sight pressure
8. Responsive layout that scales to the browser window

## Success bar
- Starts instantly in browser
- Controls feel clear
- UI fits the window
- Room can be won or lost
- The room has a real mini-arc: scout, loot, survive, escape
- Feels closer to a tactical dungeon room than a loose arcade blob
