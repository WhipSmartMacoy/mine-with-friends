# Custom sprites

Put PNG sprite sheets in this folder and list them in `sprites.json`. They load automatically for
everyone playing on your site — characters appear under **Character** in the miner creator.

Only use art you made, commissioned, or have a licence for (sprites ripped from commercial games
belong to their publishers and can't be redistributed here).

## Character sheets

Start from **`example-miner.png`** (paint over it) and use **`character-template-guide.png`** as the map —
every cell is labelled.

The sheet is **256×200 px**: 8 columns × 5 rows of **32×40** cells.

| Row | Col 0 | Col 1 | Col 2–5 | Col 6 | Col 7 |
|---|---|---|---|---|---|
| 0 – Down  | idle 1 | idle 2 | walk 1–4 | mine 1 (raise) | mine 2 (strike) |
| 1 – Left  | idle 1 | idle 2 | walk 1–4 | mine 1 | mine 2 |
| 2 – Right | idle 1 | idle 2 | walk 1–4 | mine 1 | mine 2 |
| 3 – Up    | idle 1 | idle 2 | walk 1–4 | mine 1 | mine 2 |
| 4 – Extras | wave 1 | wave 2 | hurt · sit · doze | | |

How the game uses each pose:
- **idle** loops while standing (breathing). **walk** loops while moving.
- **mine 1 → mine 2** plays on every swing.
- **wave** when you level up, forge a pickaxe or someone joins. **hurt** when a swing fails.
- **sit** after waiting ~7 s during your friend's turn. **doze** when the other player is away.

Tips: transparent background; feet sit **2 px above the bottom** of each cell; draw at 1:1 — the game
shows sheets at 2× (`"scale": 2`). Walk cycle: contact → pass (body 1 px up) → contact → pass.

Register it in `sprites.json`:

```json
{
  "characters": [
    { "id": "knight", "name": "Knight", "file": "knight.png",
      "frameWidth": 32, "frameHeight": 40, "scale": 2,
      "rows": { "down": 0, "left": 1, "right": 2, "up": 3 },
      "idle": [0, 1], "walk": [2, 3, 4, 5], "mine": [6, 7],
      "extrasRow": 4, "wave": [0, 1], "hurt": 2, "sit": 3, "doze": 4,
      "drawsTool": false }
  ]
}
```

- Set `"drawsTool": true` if your mine frames already show a pickaxe (the game then won't draw its own).
- Everything except `rows`, `idle` and `walk` is optional — missing poses fall back to standing.
- Other sizes and layouts work: change `frameWidth`/`frameHeight` and the column numbers.
  `id` may use letters, numbers, `-` and `_`; file names must end in `.png`.

## Ore nodes and stations (optional)

To replace the rocks or the cart/forge/anvil, add these to `sprites.json`:

```json
"rocks":    { "file": "example-ore.png",      "frameWidth": 32, "frameHeight": 32, "scale": 2 },
"stations": { "file": "example-stations.png", "frameWidth": 32, "frameHeight": 32, "scale": 2,
              "order": ["cart", "forge", "anvil"] }
```

- **`example-ore.png`** — 10 columns (rock level 1 Stone → 10 Mythril) × 3 rows (full, cracked, nearly gone).
- **`example-stations.png`** — 3 frames: cart, forge, anvil.
