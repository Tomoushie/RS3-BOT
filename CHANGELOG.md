# Changelog — RS3Bot

All notable changes to RS3Bot are documented here. The version follows the public release (`1.2.x`); internal milestones (V12 → V22) are noted for transparency.

## [1.3.0] — 2026-10-31 — “Market Watch & map fixes” (V17 → V22)

### Added
- **Heartbeat / online + ban foundation** (V17): free Cloudflare Worker + D1, device hash, internal online badge, graceful ban/reconnection banners; public participation is opt-in and off by default.
- **Beginner / Expert mode** (V18): beginner is the default; advanced indicators (long predictions, 80% interval, CSV, comparator, volume alert, real trades) are one click away in Settings.
- **z-score + 30-day percentile + combined signal** (V19): Buy the dip / Sell the peak / Neutral badge (Expert mode only).
- **Market Watch (premium)** (V21): post-event cycle profiles for DXP/updates, sector scores and top 8 movers (buy_dip / sell_peak / watch), optional event date with event/proxy mode.

### Changed
- Item sheet cards reorganised: Sources & cache, Real trades and Prediction under Buy limit; Alerts, Volume alert and Similar items side-by-side below the simulator.
- Submissions rows: date and price are now adjacent to the item name.
- Map mode labels no longer use emoji; nav labels vertically centred.
- **Map zoom capped at 400%** (no more black tiles at 800%).
- **Zone chips now work**: clicking Varrock / Lumbridge Swamp switches to the detailed zone and loads the map.
- Holiday ticker scrolls continuously right→left.
- PriceCheck.gg link now points to the homepage (deep links return 403); RuneStats removed (429).
- Craft recipes no longer merge alternative recipes (Cheese Wheel correctly shows only Bucket of milk).
- Window: account-delete confirmation now appears above the login screen.

### Fixed
- Tray/heartbeat/participation state leaking between Internal and Public builds.
- Premium gating remains fail-closed in Public (license required for Market Watch, Flip Planner, map, mail, comparator).

### Verification
- Rust: 83 tests passed; worker: 12 tests; E2E strict **T1→T124: 123 PASS / 0 FAIL** (621 s).
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
