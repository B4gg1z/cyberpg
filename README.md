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
- current project: CyberPG v0.1.6 one-room prototype with a cyborg kittygirl hero, original enemy silhouettes, sensible item shapes, stronger room materials, threat telegraphs, combat popoffs, reinforcements, and a post-room legacy reward loop.

## Asset / licensing posture
- current visuals are authored directly in `index.html` as HTML/CSS shapes and gradients
- no external sprite packs, marketplace art, or scraped/reference-derived game assets are bundled
- safest public path from here: keep shipping either fully original art or assets with explicit commercial redistribution rights and written provenance
