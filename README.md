# ⚜ Depths of the Dread Lich

A complete single-file roguelike dungeon crawler with 5e-inspired rules, pixel art, and a synthesized soundtrack. Descend ten floors of a cursed dungeon, brave the dark, and slay the Dread Lich Vol'tharix before he drains the world of life.

### ▶ **[Play it here → ev1lcr0w.github.io/dungeongame](https://ev1lcr0w.github.io/dungeongame/)**

No install, no accounts, no downloads — it runs in any modern browser, on desktop or phone. You can also **install it to your home screen** and play **completely offline**.

---

## The Game

You forge a hero, then descend. Every floor is generated fresh: rooms, corridors, monsters, traps, treasure, and the occasional thing that is not what it appears to be. Death is permanent (unless you're carrying a Vial of Revive), and every run is recorded in your Hall of Legends.

**Ten floors, four biomes** — the dungeon changes character as you go deeper:

| Floors | Biome | |
|---|---|---|
| 1–3 | **Stone Halls** | cold violet masonry, dust in the torchlight |
| 4–6 | **Fungal Depths** | mossy green stone, drifting spores |
| 7–9 | **Ember Reaches** | scorched brick, rising embers, dragon lairs |
| 10 | **The Lich's Sanctum** | necrotic purple, soul-wisps, and Vol'tharix |

---

## How to Play

### Controls

| Desktop | Action |
|---|---|
| `WASD` / arrow keys | Move — **walk into things to interact**: attack monsters, open doors, smash barrels, talk to prisoners |
| `Shift` + direction | **Shove** an adjacent enemy — into spike traps, through doorways, or slam them into a wall |
| Mouse click | Walk to a tile, attack a distant enemy (ranged/spells), or open a door |
| `Space` | Wait one turn |
| `Q` | Cast a spell |
| `E` | Pack & equipment (paper-doll inventory) |
| `F` | Class abilities (Rage, Second Wind, Lay on Hands…) |
| `R` | Short rest — heal by spending a hit die (only when no enemies are near) |
| `C` | Character sheet |
| `X` | **Auto-explore** — walks the floor for you, stops the instant anything appears |
| `B` | Breath weapon (Dragonborn only) |
| `O` | Options (music & effects volume) |
| `M` | Mute |
| `Enter` | Descend, while standing on the stairs |

**On mobile**, a touch d-pad and action buttons appear automatically. Tap 📊 for your character panel, 🤜 to arm a shove, then a direction.

### Your first run

1. **Forge a hero** — pick gender, difficulty, lineage, class, and roll 4d6-drop-lowest ability scores. Your class decides how you look; your race tints your color and build.
2. **Explore the floor.** Fight what you can, loot everything, smash the furniture. Watch for the **⬆ UPGRADE!** prompt — it means you just found something better than what you're wearing.
3. **Find the stairs** 🔻. Standing on them asks whether to descend or keep exploring, and tells you what you'd be leaving behind.
4. **Visit the merchant** between floors — buy gear, sell your junk, pay the blacksmith to reforge your equipment, or rest to full.
5. **Descend to floor 10** and end Vol'tharix. Then start **New Game+** and do it again, harder.

### Tips

- **Bump to interact** — nearly everything in the dungeon responds to walking into it.
- **Barrels, crates and coffins hide loot**; chests hide more, but roughly one in seven is a **Mimic**.
- **Watch the walls.** A hairline golden crack means a **hidden treasure vault** — smash through it (your hero will let you know how they feel about it).
- **Traps cut both ways.** Spotted a spike trap? Shove a goblin onto it.
- **Dragons have elemental weaknesses** — a White Dragon melts to fire, a Red Dragon shatters to frost. Carry the right scroll.
- **Rest before you descend**, not after you're in trouble.
- **The wolf is worth saving.** Free a caged wolf and it fights beside you for the whole run.

---

## Features

**Character** — 7 races × 7 classes with **multiclassing** at every level-up, ability score improvements and feats at levels 4 and 8, and 8 equipment slots on a paper-doll inventory.

**Combat** — animated d20 rolls with real 5e math: attack rolls vs. AC, critical hits, saving throws, spell slots and spell save DC, conditions (poisoned, stunned, blessed, raging, frightened), and class features from Sneak Attack to Divine Smite to Turn Undead.

**Loot** — rarity tiers (Rare / Legendary) that scale with depth, set bonuses for wearing 3+ pieces of a rarity, a blacksmith who reforges gear up to +3, elemental scrolls, and treasure goblins that flee with the good stuff.

**The dungeon** — hidden traps you spot with Wisdom and disarm with Dexterity, heavy doors that block sight until opened, secret vaults behind cracked walls, shrines and blood altars that gamble with your fate, chained prisoners who may not be prisoners, and elite champion monsters with affixes.

**Bosses** — every dragon color with its own breath weapon, resistances and taunts; Elder dragons guarding the stairs; and a three-phase final fight against Vol'tharix, who summons the dead and drains the life from anyone standing too close.

**Presentation** — pixel-art sprites, dynamic torchlight, ambient occlusion, drifting fog, weapon swing arcs, blood that stays on the floor, and a fully synthesized soundtrack that shifts between exploration, combat, and boss music — plus voice-synthesized screaming when your hero sees a dragon.

**Persistence** — mid-run saves (close the tab and continue later), a Hall of Legends recording your last 20 runs and how each one ended, 12 lifetime achievements, and a Daily Challenge that gives every player the same dungeon so you can compare runs.

---

## Difficulty & Modes

- **Easy** — enemies hit 25% softer, extra potions.
- **Normal** — the dungeon as intended.
- **Hardcore** 💀 — enemies get +20% HP and damage, and Vials of Revive do not exist. One life.
- **📅 Daily Challenge** — the dungeon is seeded from today's date, identical for everyone. Share your result from the death or victory screen.
- **🔁 New Game+** — after winning, keep your hero and descend again; enemies gain +45% HP, +1 attack and +2 damage per NG+ level. Stacks forever.

---

## Install It

On **iOS**: open the link in Safari → Share → *Add to Home Screen*.
On **Android**: open in Chrome → menu → *Install app*.
On **desktop Chrome/Edge**: click the install icon in the address bar.

You'll get a full-screen app with its own icon that works with **no internet connection**. Saves live in your browser's local storage, so each device keeps its own Hall of Legends.

---

## Running It Locally

It's a static site — no build step, no dependencies.

```bash
git clone https://github.com/Ev1lCr0w/dungeongame.git && cd dungeongame && python3 -m http.server 8000
```

Then open `http://localhost:8000/Main.html`. (Serve it over HTTP rather than opening the file directly, so the sprite sheet and service worker load correctly.)

| File | |
|---|---|
| `Main.html` | The entire game — logic, art pipeline, audio, UI |
| `tiles.png` | Sprite sheet |
| `index.html` | Redirect into the game |
| `manifest.json`, `sw.js`, `icon-*.png` | Installable-app and offline support |
| `LICENSE` | Terms of use |

---

## Credits

Pixel art: **[Dungeon Tileset II](https://0x72.itch.io/dungeontileset-ii)** by **0x72** — released under CC0 (public domain).

All music and sound effects are generated at runtime with the Web Audio API — there are no audio files.

Not affiliated with or endorsed by Wizards of the Coast. Rules are inspired by the d20 system; all names, monsters, and content here are original or generic fantasy.

## License

© 2026 Rick Farah. All rights reserved — see **[LICENSE](LICENSE)**.

Free to play and to read the source for learning. Redistributing, rehosting, selling, or publishing modified versions is not permitted without written permission. The `tiles.png` artwork is CC0 (public domain) and is not restricted by this license.
