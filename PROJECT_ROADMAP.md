# 🎮 IRON COMMAND — Project Roadmap

## What We're Building
A **base-building real-time strategy (RTS) MMO** — the same genre as Mobile Strike, Clash of Clans, and Rise of Kingdoms. Players build a military base, gather resources, train armies, research tech, form alliances, and battle other players on a shared world map.

---

## Why HTML5 + JavaScript (Web-First)

You asked about Java, standalone apps, etc. Here's the honest answer from your software expert:

**HTML5 is the BEST choice for this project.** Here's why:

| Concern | HTML5 Answer |
|---|---|
| "Can I test it easily?" | YES — open a browser on PC or phone. Done. |
| "Will it work on Android?" | YES — any phone browser. Can also wrap as a standalone Android app later (using Capacitor/PWA). |
| "Will it work on PC?" | YES — any desktop browser. Can also wrap as a desktop app (using Electron). |
| "Can it be a real game?" | YES — tons of successful MMO strategy games are web-based. |
| "Good graphics?" | YES — HTML5 Canvas + WebGL can do beautiful 2D art. |
| "Multiplayer?" | YES — WebSockets are the standard for real-time web multiplayer. |
| "Secure?" | YES — server-authoritative architecture keeps cheaters out. |
| "Do I need a Mac?" | NO — everything works on Windows + Android. |

**The tech stack (what we'll use):**
- **Game UI & Rendering**: HTML5 + CSS + JavaScript (vanilla first, libraries later)
- **Game Framework** (Stage 3+): Phaser.js or PixiJS for world map rendering
- **Backend Server** (Stage 5+): Node.js + Express + WebSocket
- **Database** (Stage 5+): PostgreSQL for game state persistence
- **Authentication** (Stage 6+): JWT tokens, OAuth (Google login)
- **Android App**: Progressive Web App (PWA) or Apache Capacitor wrapper
- **Desktop App**: Electron wrapper (optional — browser works fine)

---

## Development Stages

### ✅ STAGE 1 — Base Building Foundation
**Goal**: A playable single-player base screen with buildings, resources, and timers.

Features:
- Base grid view with placeable building plots
- 5 building types: Command Center, Farm, Iron Mine, Barracks, Warehouse
- 3 resources: Gold, Food, Iron (with passive generation)
- Construction timers (build and upgrade buildings)
- Building levels (1-5 for Stage 1)
- Resource bar UI at the top
- Building info panel on tap/click
- Mobile-responsive (works on phone browsers)
- Save/load game state (localStorage)

**How to test**: Open the HTML file in Chrome on PC or Android. That's it.

---

### ✅ STAGE 2 — Research & Progression
**Goal**: Add depth with a tech tree and more meaningful upgrades.

Features:
- ✅ Research Lab building
- ✅ Tech tree with 3 branches (Economy, Military, Defense)
- ✅ Research timers
- ✅ Tech unlocks that boost stats (faster resource gen, stronger troops)
- ✅ Commander/hero profile with level + XP
- ✅ Daily login rewards system
- ✅ Quest/mission system (build X, upgrade Y)
- ✅ Notifications for completed timers

---

### ✅ STAGE 3 — Army & Combat (PvE)
**Goal**: Train troops and fight AI enemies.

Features:
- ✅ Troop types: Infantry, Vehicles, Artillery, Air Support
- ✅ Troop training (costs resources + time, bulk train ×5)
- ✅ Army composition screen (3 tabs: Troops, Train, Hospital)
- ✅ PvE campaign map with 15 AI missions
- ✅ Auto-battle combat system (multi-round, research bonuses)
- ✅ Combat reports with detailed battle logs
- ✅ Loot from victories (resources + XP)
- ✅ Hospital system (heal wounded troops over time)
- ✅ Combat-related quests

---

### ✅ STAGE 4 — World Map & Exploration
**Goal**: A zoomable world map with resource tiles and NPC bases.

Features:
- ✅ Canvas-based 40×40 tile world map with pan/zoom
- ✅ Resource tiles to occupy (gold, food, iron income)
- ✅ 5 NPC rebel base types to raid (scattered by distance)
- ✅ Fog of war / scouting (reveal on march + defeats)
- ✅ March system (send troops with travel time, max 3 marches)
- ✅ Map coordinates display and home button
- ✅ Legend panel and tile info on tap

---

### ✅ STAGE 5 — Enhanced Persistence & Polish
**Goal**: Save slots, data portability, achievements, sound, and QoL improvements.

Features:
- ✅ 3 Save Slots with preview (HQ level, power, commander, last played)
- ✅ Export/Import saves (base64 code for cross-device transfer)
- ✅ Auto-backup (previous save preserved, restore in settings)
- ✅ 18 Achievements with permanent tracking and unlock badges
- ✅ Sound effects (Web Audio API — build, research, battle, achievement, UI)
- ✅ Sound on/off toggle in settings
- ✅ Old save migration (v1-v4 auto-migrated to Slot 1)
- ✅ Per-slot and global reset (type RESET to confirm)
- ✅ Slot deletion from main menu

---

### ✅ STAGE 6 — Gameplay Depth & Visual Polish
**Goal**: Gems economy, heroes, events, alliance, particles, tutorial.

Features:
- ✅ Gems premium currency (earn from achievements, daily login, events)
- ✅ Speed-up system (instant-finish any timer with gems)
- ✅ 8 recruitable Heroes with passive bonuses (+ATK, build speed, research, gather, heal, power)
- ✅ Hero equip system (one active hero at a time)
- ✅ 3 timed events (Resource Rush, War Games, Raid Boss)
- ✅ Raid Boss: deal damage with troops, claim rewards when killed
- ✅ Event bonuses: doubled production or doubled battle rewards
- ✅ Alliance placeholder (create name/tag/icon, solo prep for multiplayer)
- ✅ Canvas particle effects (gold, red, purple, cyan sparkles)
- ✅ 6-step interactive tutorial for new players
- ✅ Gems in resource bar (tap for gem shop)
- ✅ Heroes/Events in fan menus, Alliance in Profile

---

### 🔲 STAGE 7 — Polish & Monetization
**Goal**: Make it feel like a real, polished game.

Features:
- Sound effects and music
- Particle effects and animations
- Notification system (push notifications on mobile)
- In-game mail system
- Premium currency (Gems/Gold) and shop
- Speed-up items
- VIP system
- Events (time-limited challenges with rewards)
- Seasonal content

---

### 🔲 STAGE 8 — Standalone Apps & Distribution
**Goal**: Package as real apps and distribute.

Features:
- Progressive Web App (PWA) — installable from browser
- Android APK via Apache Capacitor
- Desktop app via Electron (optional)
- Publish to Google Play Store
- Landing page / website
- Terms of service, privacy policy
- Analytics and crash reporting

---

## File Structure (planned)

```
iron-command/
├── PROJECT_ROADMAP.md          ← You are here
├── CHANGELOG.md                ← What changed each version
│
├── client/                     ← All frontend game code
│   ├── index.html              ← Main game entry point
│   ├── css/
│   │   ├── main.css
│   │   ├── buildings.css
│   │   └── ui.css
│   ├── js/
│   │   ├── game.js             ← Core game loop
│   │   ├── buildings.js        ← Building definitions & logic
│   │   ├── resources.js        ← Resource system
│   │   ├── timers.js           ← Construction/training timers
│   │   ├── ui.js               ← UI rendering & interactions
│   │   ├── save.js             ← Save/load system
│   │   └── config.js           ← Game balance constants
│   └── assets/
│       ├── icons/
│       ├── sprites/
│       └── audio/
│
├── server/                     ← Backend (Stage 5+)
│   ├── index.js
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   └── websocket/
│
└── docs/                       ← Game design documents
    ├── GAME_DESIGN.md
    ├── BALANCE_SHEET.md
    └── API_SPEC.md
```

---

## Current Status

| Stage | Status | Version |
|---|---|---|
| Stage 1 — Base Building | ✅ Complete | v0.1.0 |
| Stage 2 — Research & Quests | ✅ Complete | v0.2.0 |
| Stage 3 — Army & Combat | ✅ Complete | v0.3.0 |
| Stage 3 — Army & Combat | ✅ Complete | v0.3.0 |
| Stage 4 — World Map | ✅ Complete | v0.4.0 |
| Stage 5 — Persistence & Polish | ✅ Complete | v0.5.0 |
| Stage 6 — Depth & Polish | ✅ Complete | v0.6.0 |
| Stage 7 — Polish | ⬜ Not started | — |
| Stage 8 — Distribution | ⬜ Not started | — |

---

*Last updated: February 19, 2026*
*Project codename: Iron Command*
