# CyberPG

A fresh reboot of CyberPG as a **Shattered Pixel Dungeon-inspired** prototype.

## Current goal
Build a **one-room playable test slice** before expanding scope.

## Prototype rules
- Browser-first
- Turn-based grid movement
- One authored room only
- Melee bump combat
- Readable UI and combat log
- Finish the room by beating enemies and reaching the exit

## Controls
- `WASD` or arrow keys: move / attack
- `Space`: wait a turn
- `R`: restart the room

## Run locally
Open `index.html` directly in a browser, or serve the folder:

```bash
cd /Users/baggis/Documents/CyberPG
python3 -m http.server 8766
```

Then open:

- `http://127.0.0.1:8766/`

## Design target from research
Shattered Pixel Dungeon feel to chase in the reboot:
- small readable room-scale tactical decisions
- turn-based movement where positioning matters
- clean bump combat
- dangerous but understandable enemies
- item pickup / healing / exit pressure
- strong tile readability over flashy effects

## Current status
- current project: CyberPG v0.1.4 one-room prototype with fog-of-war, threat telegraphs, combat popoffs, alarm reinforcements, and a post-room legacy reward choice for the next run.
