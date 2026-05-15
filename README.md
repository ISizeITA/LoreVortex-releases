# Loreforge

A **peer-to-peer** desktop companion for tabletop RPGs (D&D 5e, Pathfinder, Call of Cthulhu, custom systems). Dark fantasy theme, Italian / English, two roles: **Game Master** and **Player**.

> This repository hosts the public installers. The source code is private and proprietary.

---

## Download

**[Get the latest installer →](https://github.com/ISizeITA/LoreForge-releases/releases/latest)**

1. Download `Loreforge_x.x.x_x64-setup.exe` from the latest release.
2. Double-click and click through the installer.
3. Launch Loreforge from the Start menu.

You do **not** need Node.js, Python, a terminal, or any developer tools. Loreforge is a native Windows app — just download and run.

**Requirements:** Windows 10 or 11 with WebView2 (preinstalled on up-to-date systems; the installer configures it if missing).

---

## Updates

From the start screen, click **"Check for updates"**. When a newer version is available you'll see *"Install and restart"* — Loreforge downloads the signed update, installs it, and relaunches itself.

Every update is cryptographically verified against the maintainer's private signing key before installing; tampered or third-party builds are rejected.

---

## What it does

- **Interactive map** — image + grid (square or hex), draggable tokens, obstacles (walls, crates, trees), **fog of war** with real line-of-sight that reacts to time of day and weather, **multi-map** with a bottom switcher, optional **snap-to-grid**, **ping tool** for calling attention.
- **Tokens** — custom image, HP / max HP with % overlay, **12 status conditions**, per-player ownership, lock/hide.
- **P2P lobby** — direct WebRTC connection (offer/answer copy-paste), **optional session password**, **graceful reconnection**.
- **Time & weather** — in-game clock on a seasonal dial; random weather per biome and season that can reduce vision in the fog of war.
- **Dice** — d4/d6/d8/d10/d12/d20/d100 with quantity + modifier and a shared roll log.
- **Initiative** — turn order with HP and sides.
- **Character cards** — D&D 5e / Pathfinder / Call of Cthulhu presets or custom stats.
- **Notes, narrative, chat** — private notes per player, GM narrative panel, group chat.
- **NPCs** — generator with preset races + shared library with descriptions, portraits, notes.
- **PDF reader** — load your rulebook inside the app, with text search.
- **Embedded browser** — quick web lookups without leaving the app.
- **Music** — shared playlist + synced player with P2P file transfer.

---

## How it works

100% peer-to-peer over WebRTC: no central server, no account, no telemetry. The GM creates an invite, sends it to a player out-of-band (Discord, email, anything), the player replies. From there the connection is **direct, PC-to-PC**, and session state is synchronized with **Yjs CRDTs** so there are no conflicts.

The GM's machine acts as the session host. Players talk to the GM and the GM rebroadcasts to the others (star topology). Local state is persisted by the GM in SQLite.

---

## License

Loreforge is **proprietary software** — all rights reserved.

The installer is **free to download and use for personal tabletop play**. You may **not** redistribute, decompile, reverse-engineer, modify, or reuse the application or its assets for any purpose without explicit written permission from the maintainer.

The source code is **not** open source and is not available for review or copying.

For licensing inquiries, contact the maintainer through this repository's issue tracker.
