# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a collection of browser-based games built as single self-contained HTML files. No build system, no dependencies, no package manager — open any `.html` file directly in a browser to run it.

## Running Games

```bash
open tictactoe.html
open flappybatman.html
```

Or serve locally to avoid any browser file restrictions:

```bash
python3 -m http.server 8080
```

## Architecture

Each game is a **single HTML file** with all CSS and JavaScript inline. This is intentional — no external files, no imports, no bundling needed.

**tictactoe.html** — Two-player Tic Tac Toe. Game state is held in plain JS variables (`board`, `current`, `over`, `scores`). Win detection uses a hardcoded `WINS` array of index triples.

**flappybatman.html** — Canvas-based Flappy Bird clone with a Batman theme. Uses `requestAnimationFrame` for the game loop. State machine with three modes: `idle`, `play`, `dead`. Batman is drawn procedurally with Canvas 2D API (no sprites).

## Deployment

All changes should be committed and pushed to GitHub after every modification:

```bash
git add <file>
git commit -m "description"
git push origin main
```

Remote: `https://github.com/GuyFromThePost28/cluadecode`
