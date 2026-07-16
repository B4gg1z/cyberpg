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
- Click / tap an adjacent tile: move / attack
- Hover a visible tile: preview route and target readout
- Click / tap a distant visible tile: lock the route preview
- Click that locked route again: advance one turn along it
- Multi-step route previews now call out whether the **first committed step** is threatened
- Adjacent enemy previews now show attack range / kill odds
- `F`: use a stored heal flask charge
- `Space`: wait a turn
- Hover your own tile or read the wait button to see whether holding position is safe this turn
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
- current project: CyberPG v0.1.22 one-room prototype with a cyborg kittygirl hero, readable enemy badges/silhouettes, stronger chest/sigil payoff, explicit Volt Fang drop/pickup flow, combat-preview landing threat warnings, first-step route danger warnings for click-again movement commitment, attack-range / kill-odds inspect text, on-board enemy intent badges with damage callouts, a gold pulse marker for the live room objective, an objective route readout with step count / first-step safety / seen state, click-again route commitment, last-seen enemy ghost memory, manual heal flask inventory/use, a heavier heal-flask payoff that can actually swing the first room, truthful hold-position danger readouts on the hero tile and wait button, hunter rush telegraphs plus a real two-tile rush carve, richer in-room environment dressing with vents/cables/terminals/crates/coolant, better combat outcome readability, a cleaner public-demo shell, and mouse/touch route preview controls.

## Asset / licensing posture
- current visuals are authored directly in `index.html` as HTML/CSS shapes and gradients
- no external sprite packs, marketplace art, or scraped/reference-derived game assets are bundled
- safest public path from here: keep shipping either fully original art or assets with explicit commercial redistribution rights and written provenance
