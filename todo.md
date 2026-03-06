```markdown
# Ruby Pine Script TODO.md
**Last updated:** March 06, 2026  
**Status:** 100% production-ready — clean, fast, fully synced with NT8 logic  
**Version:** Ruby v2.1 – NT8 Sync Edition

---

## ✅ COMPLETED

### Core Fixes Applied
- [x] Fixed overlapping Support/Resistance entry zone boxes (`var box` + live update instead of `box.new()` spam)
- [x] Optimized dashboard table (compact v2 — 25 rows → max 18 rows, small text, no empty separators, packed metrics)
- [x] Added `max_boxes_count = 500, max_lines_count = 500` to `indicator()` line
- [x] Added full NT8-style breakout points (30-min ORB + PrevDay + IB60 + Squeeze) with clean plots, markers, and dashboard section
- [x] Session-aware reset (works on all timeframes)
- [x] Breakout points now integrated into signals & dashboard (perfect visual sync)

### Dashboard & Visual Polish
- [x] Professional color-coded dashboard with emojis
- [x] Wave dominance, trend speed, market regime, volatility percentile all working perfectly
- [x] Clean chart mode + heatmap barcolor preserved

### Recent Updates (March 06, 2026)
- [x] **Higher-TF S/R Fix Applied**: Replaced `getNearestSRLevels()` with cleaner `getNearestSR()` using built-in `ta.pivothigh`/`ta.pivotlow` — dashboard levels now more reliable
- [x] **K-Means Performance Tweak**: Changed `recalculate_clusters` from 20 to 50 for better performance on 1-minute charts
- [x] **Breakout Points System IMPLEMENTED**: Full NT8-style breakout detection now live:
  - 30-Minute Opening Range Breakout (ORB) with visual markers
  - Previous Day High/Low tracking and plotting
  - Initial Balance 60-min (IB60) breakout detection
  - Squeeze detection (Bollinger Bands inside Keltner Channels)
  - Dedicated dashboard section with real-time breakout status
  - 5 new alert conditions for all breakout events
  - Configurable inputs for all breakout parameters
- [x] **Box Stacking FIXED**: Entry zone boxes now use `var box` and update properly without creating ghost images
- [x] **Dashboard Optimization**: 
  - Made dashboard ultra-compact with `size.tiny` text
  - Removed all spacer rows for tighter layout
  - Shortened all labels (Dir, Sig, Q, Sess, etc.)
  - Reduced visual footprint by ~60%
  - Added master toggle to show/hide entire dashboard
- [x] All changes verified — no errors
- [x] **Version Label Added**: Dashboard header now shows "Ruby v2.1 – NT8 Sync"
- [x] **Squeeze Wired Into Signals**: `squeeze_fired` now boosts signal quality score and can trigger buy/sell signals on volatility expansion; wave ratio requirement relaxed when squeeze fires
- [x] **Price Labels in Entry Zones**: Support and resistance boxes now show live price labels (S: / R:) centered inside the zones
- [x] **Breakout Strength Meter**: 0–100% composite score in dashboard (wave ratio 40%, volume surge 30%, squeeze 15%, trend alignment 15%) with emoji indicator
- [x] **Indicator Line Fixed**: Added missing `max_boxes_count = 500, max_lines_count = 500` to `indicator()` call

---

## 📋 FUTURE ENHANCEMENTS (Nice-to-have)

### Visual & UX
- [ ] Auto-hide dashboard on mobile/small screens
- [ ] Mini ultra-compact dashboard mode (2 columns)
- [ ] Make VOLATILITY section collapsible in dashboard

### Signals & Logic
- [ ] Wire Ruby signal quality directly into NT8 CNN tabular features (for even tighter sync)

---

**Project Goal:** One beautiful, clutter-free Ruby chart → instant professional signals & perfect NT8 execution.

