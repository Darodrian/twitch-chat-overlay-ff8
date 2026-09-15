# Twitch Chat Overlay (FF8 edition)

A Twitch chat overlay for OBS styled after Final Fantasy VIII's UI: warm stone message boxes that pop into existence at their final size, with the in-game bitmap font rendered from a sprite atlas (`ff8-font.png`).

## Features

- FF8 stone-block message boxes with a center pop-in animation
- Typewriter text that fills a pre-sized box (box already knows its final footprint)
- Bitmap font glyphs drawn to `<canvas>` at native resolution and pixel-scaled 2x — crisp, no inter-glyph bleed
- Smart quotes: `"..."` and `'...'` automatically render as curly `"..."` / `'...'` using the FF8 glyphs
- Names tinted by role using FF8 color rows: broadcaster (yellow), mod, VIP (pink), subscriber
- BTTV, 7TV, Twitch emotes and FFZ emote modifiers
- Zero-width overlay emotes stack on the previous emote
- `F` key toggles the FF8 layout tuner (line height, vertical nudges, band trims)

## Setup

1. Edit `channel.js` and set your Twitch channel:

   ```js
   var CHANNEL = "yourchannel";
   ```

2. Open `index.html` directly in a browser, or add it to OBS as a **Browser Source**.

## GitHub Pages

1. Push this repo to GitHub.
2. In the repo: **Settings → Pages → "Deploy from a branch" → Branch: `main`, folder: `/root` → Save**.
3. Use `https://<user>.github.io/twitch-chat-overlay-ff8/` as your OBS Browser Source URL.

## Credits

- `zpix.woff2` — Zpix (最像素) pixel font by SolidZORO, free for personal use — https://github.com/SolidZORO/zpix-pixel-font (fallback for characters missing from the sprite atlas)
- `ff8-font.png` — sprite glyph atlas sourced from the game's UI font