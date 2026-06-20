# Chromatik

A fast, colorful memory game for the browser. Chromatik flashes a growing sequence of glowing tiles and challenges you to repeat it back. One wrong tile and you start over, so how far can your memory take you?

**Play it live:** https://quickie-game.vercel.app

## How to Play

1. Press any key to start the game.
2. Watch carefully. The board flashes one tile and plays a tone.
3. Click the tiles in the exact same order you just saw.
4. Clear a round and the sequence grows by one tile, bumping you to the next level.
5. Make a mistake and the screen flashes red, the game ends, and you press any key to try again.

The goal is simple: reach the highest level you can before your memory slips.

## Features

- Four glowing color tiles, each with its own tone.
- Endless levels that grow one step at a time.
- Retro arcade styling with the "Press Start 2P" pixel font.
- Instant restart, no menus or loading screens.

## Tech Stack

- Vanilla HTML, CSS, and JavaScript.
- jQuery for DOM updates and animations, loaded from a CDN and pinned with a Subresource Integrity (SRI) hash.
- No build step and no backend. It is a fully static, client-side game.

## Run It Locally

Because the game loads sound files, open it through a small local web server rather than the `file://` protocol.

```bash
# Clone the repository
git clone https://github.com/ShAuRyA-Noodle/Chromatik.git
cd Chromatik

# Start any static server, for example:
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

## Project Structure

```
index.html     Game markup and CDN script tags
styles.css     Layout, colors, and animations
game.js        Game logic (sequence generation, input checking, scoring)
sounds/        Tile and game-over audio clips
```

## Security

- The jQuery CDN script is pinned with an SRI hash and `crossorigin="anonymous"` to prevent tampered third-party code from running.
- CodeQL static analysis and Dependabot run on the repository.
- See [SECURITY.md](SECURITY.md) for how to report a vulnerability.

## Credits

Built by Shaurya. The Simon-style memory game concept is a long-standing classic; this is an original implementation with custom styling.
