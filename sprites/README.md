# Custom sprites

Put PNG sprite sheets in this folder and list them in `sprites.json`. They load automatically for
everyone playing on your site — characters appear under **Character** in the miner creator.

Only use art you made, commissioned, or have a licence for (sprites ripped from commercial games
belong to their publishers and can't be redistributed here).

## Character sheets

Start from **`example-miner.png`** (paint over it) and use **`character-template-guide.png`** as the map.

| | Column 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| **Row 0** | down – idle | walk 1 | walk 2 | walk 3 | walk 4 |
| **Row 1** | left – idle | … | | | |
| **Row 2** | right – idle | … | | | |
| **Row 3** | up – idle | … | | | |

- Each cell is **32×40 px** (the whole sheet is 160×160). Transparent background.
- Feet sit **2 px above the bottom** of each cell; the game stands the character on that line.
- Walk cycle: contact → pass (body 1 px up) → contact with the other foot → pass.
- Draw at 1 pixel = 1 pixel. The game shows sheets at 2× (`"scale": 2`).

Add it to `sprites.json`:

```json
{
  "characters": [
    { "id": "knight", "name": "Knight", "file": "knight.png",
      "frameWidth": 32, "frameHeight": 40, "scale": 2,
      "rows": { "down": 0, "left": 1, "right": 2, "up": 3 }, "idle": 0, "walk": [1, 2, 3, 4] }
  ]
}
```

Different sizes work too — change `frameWidth`/`frameHeight`. Different layouts work by changing
`rows`, `idle` and `walk` (column numbers; any number of walk frames). `id` may use letters,
numbers, `-` and `_`; file names must end in `.png`.

## Ore nodes and stations (optional)

To replace the rocks or the cart/forge/anvil, add these to `sprites.json`:

```json
"rocks":    { "file": "example-ore.png",      "frameWidth": 32, "frameHeight": 32, "scale": 2 },
"stations": { "file": "example-stations.png", "frameWidth": 32, "frameHeight": 32, "scale": 2,
              "order": ["cart", "forge", "anvil"] }
```

- **`example-ore.png`** — 10 columns (rock level 1 Stone → 10 Mythril) × 3 rows (full, cracked, nearly gone).
- **`example-stations.png`** — 3 frames: cart, forge, anvil.
