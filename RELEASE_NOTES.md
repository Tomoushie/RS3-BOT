# RS3Bot v1.3.1 — Mean-reverting forecasts

**Track prices. Spot flips. Trade smarter.**

RS3Bot is a native Windows app for the RuneScape 3 Grand Exchange: 33,778 items, multi-source prices, price history with predictions, Flip Score, liquidity, alchemy, buy-limit tracking, local trade journal, interactive map and premium Market Watch.

### Download
- `RS3Bot_1.3.1_x64-setup.exe` — recommended installer
- `RS3Bot_1.3.1_x64_en-US.msi` — MSI package
- `rs3-grand-market.exe` — portable executable

### What’s new in 1.3.1
- **Long-term forecasts fixed**: J+7/J+30 keep OLS; J+90/J+180 now use an Ornstein-Uhlenbeck mean-reversion blend (30-day equilibrium mean) instead of extrapolating the latest slope. Cheese J+90 ≈ 1 876 po (was 3 499), J+180 ≈ 1 861 po (was 5 075).
- **Prediction card fixed**: the item sheet “Prediction & trend” card now renders the backend horizons; the stale local OLS values are gone.
- **History enrichment**: `get_predictions` fills a short local history with Weirdgloop last90d (cached 10 min), so the long-term model has enough context.
- **Intervals**: 80% long-term intervals are capped to the known historical price envelope (no more confidence above the all-time high).

### Requirements
Windows 10/11 (x64). Internet connection for prices. Read-only analysis — no game account access, no automation.

> Windows SmartScreen may warn because the binary is not code-signed. Use *More info → Run anyway*, and verify the SHA-256 checksums.

**Not affiliated with Jagex Ltd.**
