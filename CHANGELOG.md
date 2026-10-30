# Changelog — RS3Bot

All notable changes to RS3Bot are documented here. The version follows the public release (`1.2.x`); internal milestones (V12 → V16) are noted for transparency.

## [1.2.0] — 2026-10-30 — “Grand Exchange Intelligence” (V16)

### Added
- **Premium offline licensing**: Ed25519-signed license keys, local activation, device binding option, activation modal and Settings licence row.
- **Backend fail-closed premium gating**: premium data commands refuse to serve data in the public build without a valid license (no more JS-only lock).
- **Flip Planner** (premium): 3–5 best flips from capital, available time and risk tolerance, ranked by net profit per 4-hour buy-limit window.
- **Item analysis upgrades**: prediction line overlaid on the price chart with 80% interval, liquidity badge, 30-day range position, recent 10-trade price, Flip Score, alchemy and buy-limit tools.
- **Trade journal**: notes, win rate, realised profit, performance by item category.
- **Interactive map**: 167 curated locations (banks, mines, fishing, farms, altars, shops, slayer masters, teleports), dynamic layers, search and popups; dungeon/zone viewer.
- **Local profiles**: optional multiple local accounts with PIN protection and data isolation.
- **Privacy & comfort**: 100% local data, notifications toggle, system tray with minimise/quit prompt, custom cursor, seasonal themes, French/English UI.
- **Security hardening**: salted PIN hashes, AES-GCM encrypted “remember me”, anti-bruteforce lock, offline licence verification.

### Changed
- Complete Rust backend refactor (modular `model/http/cache/wiki/refresh/ge/alerts/extras/diagnostics/maps/planner/premium`), 65 backend commands, 71 Rust tests.
- Full E2E suite (100+ checks) covering navigation, catalogue, item pages, alerts, journal, bank, map, comparator, mail, accessibility and licensing.

### Fixed
- Item page header overflow on wide screens (buttons now wrap cleanly below the title).
- Favourites table column alignment.
- Bank autocomplete now understands French item names (e.g. “fromage” → Cheese).
- Footer simplified (status moved into the online pill, licence/version in Settings).

## [1.0.0] — 2026-10-27
- Initial public foundation: Tauri shell, catalogue, item pages, alerts, calculators, first-run tutorial.

---

_Roadmap: OSRS dataset, full underground map coverage, Keyforge/cloud licences, early access._
