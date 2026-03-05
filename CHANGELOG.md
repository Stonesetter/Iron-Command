# CHANGELOG — Iron Command

## v0.6.0 — Stage 6: Gameplay Depth & Visual Polish (Feb 20, 2026)

### Added — 💎 Gems Premium Currency
- New resource displayed in resource bar (tap for Gem Shop)
- Earn gems from: achievements (+5 each), daily login (+2/day), events (+8-15), tutorial completion (+5)
- New games start with 10 gems
- Gem Shop shows all active timers with instant-finish cost (1 gem per minute remaining)
- Speed-up buttons for: construction, research, training queue, marches
- Tracks total gems earned/spent in stats

### Added — 🦸 Hero System (8 Heroes)
- **Sgt. Reeves** (Common) — +5% Army ATK | Free at HQ 1
- **Chief Engineer** (Common) — -10% Build Time | 💎50, HQ 2
- **Dr. Voss** (Rare) — -15% Research Time | 💎100, HQ 3
- **Quartermaster** (Rare) — +12% Resource Rate | 💎150, HQ 4
- **Ghost** (Epic) — +15% Army ATK | 💎250, HQ 5
- **Doc Mercy** (Epic) — +25% Hospital Heal Rate | 💎350, HQ 6
- **Gen. Ironclad** (Legendary) — +8% All Combat Stats | 💎500, HQ 8
- **Warlord Kaine** (Legendary) — +10% Total Power | 💎750, HQ 10
- Equip one hero at a time — bonuses apply globally
- Hero panel accessible from Military fan menu
- Rarity color-coded: common (gray), rare (blue), epic (purple), legendary (gold)
- Locked heroes show HQ requirement, unlocked show recruit cost
- Particle effects on recruit

### Added — ⏱️ Timed Events (3 Types)
- **Resource Rush** (1hr) — All production doubled, rewards: 2000g/1500f/1000i + 💎10
- **War Games** (1hr) — Battle rewards doubled, rewards: 1500g/1000f/800i + 💎8
- **Raid Boss: Titan** (2hr) — Send troops to deal damage, boss has 10,000 HP
  - Attack uses all troops, 10-20% casualties per attack
  - Damage based on army strength with variance
  - Kill boss to claim rewards: 3000g/2000f/1500i + 💎15
  - Progress bar shows boss HP remaining
- Start events from Events panel (World fan menu)
- One event active at a time
- Event notification dot on World fan

### Added — 🏰 Alliance System (Placeholder)
- Create an alliance: choose name, tag (2-4 letters), and icon (10 options)
- Alliance banner displays in profile
- Solo prep for future multiplayer
- Disband option
- Accessible from Profile fan menu
- Future features listed: chat, rally attacks, territory, wars

### Added — ✨ Particle Effects
- Canvas-based particle system (runs on separate canvas layer)
- Particle bursts on: hero recruit (purple), event claim (gold), alliance creation (cyan), raid boss hit (red), achievement unlock (gold)
- 6 color palettes: gold, red, green, purple, cyan, blue
- Physics: gravity, velocity, fade-out lifecycle

### Added — 📖 Tutorial System
- 6-step guided tutorial for new games:
  1. Welcome, Commander! (overview)
  2. Build Your Base (resource buildings)
  3. Research & Train (lab + barracks)
  4. Explore the World (map + occupation)
  5. Gems & Heroes (economy)
  6. Ready to Command! (send-off)
- Overlay with step counter, icon, description
- Awards 💎5 gems on completion
- Only triggers on new game (not on load)

### Changed — Hero Bonuses Applied Everywhere
- ATK/DEF/HP bonuses integrated into calcArmyStrength
- Build speed bonus reduces construction time (bTime)
- Research speed bonus reduces tech time (techTime)
- Gather bonus multiplies all resource production rates
- Heal rate bonus increases hospital heal speed
- Power bonus scales total power display
- Event production bonus multiplies resource rates
- Event battle reward bonus scales campaign loot

### Changed — UI Updates
- Resource bar: added 💎 Gems display (tap for shop)
- Military fan: added 🦸 Heroes
- World fan: added ⏱️ Events (with notification dot)
- Profile fan: 🏰 Alliance replaces locked "Clan" placeholder
- Stats panel: new Economy section (gems, hero, alliance)
- Settings: version updated to v0.6.0
- Save format v6 (auto-loads from v5 and older)

### Bug Fixes
- Hero bonuses now properly default to 0 when no hero equipped
- Event bonus returns 1 (no effect) when no event active or expired
- Particles canvas uses pointer-events:none (doesn't block clicks)
- Tutorial overlay at z-index 800 (above all game UI)

---

## v0.5.0 — Stage 5: Enhanced Persistence & Polish
- 3 save slots, export/import, auto-backup, 18 achievements, sound effects

## v0.4.1 — UI Overhaul: Main Menu, Fan Menus & Settings
- Main menu, fan popup menus, settings with bulletproof reset

## v0.4.0 — Stage 4: World Map & Exploration
- Canvas 40×40 world map, fog of war, resource tiles, NPC bases, marches

## v0.3.0 — Stage 3: Army & Combat PvE
- 4 troop types, 15-mission campaign, auto-battle, hospital

## v0.2.0 — Stage 2: Research, Commander & Quests
- Research Lab, Tech Tree, Commander XP, quests, daily login

## v0.1.0 — Stage 1: Base Building Foundation
- 4x4 base grid, 8 buildings, 3 resources, save/load
