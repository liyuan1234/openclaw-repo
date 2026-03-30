# openclaw-repo

A tiny static arcade with two browser-playable experiences:

- **Neon Pong** — a polished browser-based Pong game
- **Dungeon Bot** — a Telegram-style text adventure game

## Included apps

### 1) OpenClaw Arcade launcher
Open `index.html` to get a simple landing page with links to both games.

### 2) Neon Pong
Features:
- Neon arcade styling
- Solo mode against a simple AI opponent
- Two-player local mode
- Scoreboard with win condition (first to 7)
- Pause and instant restart controls
- Local browser persistence for scoreboard state and match stats

Controls:
- `W` / `S` — left paddle
- `↑` / `↓` — right paddle
- `A` — toggle AI / two-player mode
- `P` — pause
- `Space` — start or restart the match

### 3) Dungeon Bot
A text-based adventure presented like a Telegram bot chat.

Features:
- Local browser save and restore for the current run
- Chat history persists across refreshes

Commands:
- `/start` — reset the run
- `/explore` — search for enemies, treasure, or events
- `/fight` — attack an active enemy encounter
- `/rest` — recover HP when safe
- `/inventory` — show gear and resources
- `/drink` — use a healing potion
- `/help` — show the command list

## Run

Open `index.html` directly in a browser.

Or serve it locally:

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Files

- `index.html` — landing page / launcher
- `pong.html` — Pong game
- `telegram-quest.html` — Telegram-style text adventure

## Persistence

Both games now store progress in browser `localStorage`:

- `pong.html` remembers the current scoreboard, selected mode, and browser-local match stats
- `telegram-quest.html` restores the current dungeon run and chat history after a refresh
