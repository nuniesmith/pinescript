# Ruby v1.0

**All-in-one professional trading indicator for TradingView (Pine Script v6)**

Ruby combines trend speed analysis, wave dominance tracking, multi-timeframe support/resistance, K-Means adaptive volatility, and 
breakout detection into a single clean overlay — with a compact real-time dashboard that tells you everything at a glance.

---

## Features

### Trend Speed & Wave Analysis
- Dynamic EMA with acceleration-adjusted alpha — adapts to momentum shifts in real time
- Wave dominance ratio tracking (bull vs. bear wave size) with historical comparison
- Asset-specific presets for Gold, Crypto, Stocks, and Forex
- Trend direction, current wave ratio, and market bias all surfaced in the dashboard

### Signal Engine
- **Quality-scored buy/sell signals** — each signal rated 0–100% based on volatility, momentum, trend speed, S/R bias, and squeeze state
- Bullish & bearish candle pattern detection (hammer, engulfing, pin bar)
- Configurable cooldown between signals to avoid overtrading
- Optional volume filter and trend alignment requirements
- Entry labels with price, stop-loss, quality %, and wave ratio printed directly on chart

### Breakout Points
- **30-Minute Opening Range Breakout (ORB)** — high/low plotted with directional markers
- **Previous Day High/Low** — step-line reference levels
- **Initial Balance (60-min)** — IB range with breakout detection
- **Squeeze Detection** — Bollinger Bands inside Keltner Channels, fires on expansion
- **Breakout Strength Meter** — 0–100% composite score (wave ratio, volume surge, squeeze, trend alignment) displayed in dashboard
- Squeeze breakouts wired directly into the signal engine for stronger confluence

### Support / Resistance
- Multi-timeframe S/R via `ta.pivothigh` / `ta.pivotlow` (1-min and 5-min)
- Directional bias (Long / Short / Neutral) per timeframe shown in dashboard
- Visual entry zone boxes with live price labels (S: / R:) centered inside

### Volatility Analysis
- **K-Means Adaptive ATR** — 3-cluster unsupervised classification (High / Medium / Low) recalculated every N bars
- Volatility percentile ranking with regime labels (Very Low → Very High)
- Automatic stop-loss scaling based on volatility cluster and market phase
- Strategy suggestions in dashboard (AVOID / WIDE / TIGHT / BRKOUT / NORM)

### Market Regime & Phase
- Regime detection: Trending Bull, Trending Bear, Volatile, Ranging, Neutral
- Market phase tracking: Uptrend, Downtrend, Accumulation, Distribution
- RSI integration for phase confirmation
- Higher-timeframe MA trend filter (configurable: 15m to Daily)

### Dashboard
- Compact color-coded table with emoji indicators
- Togglable sections: Trend, Wave, Regime, Breakouts, S/R, Volatility
- Dark / Light theme support
- Movable to any corner
- Master show/hide toggle

### Visuals
- Weather heatmap barcolor (regression-based temperature gradient)
- Support / Resistance / Mid bands
- Optional ATR bands, potential signal diamonds, session background shading
- Clean Chart Mode to hide all bands and show only signals

---

## Alerts

| Alert | Description |
|-------|-------------|
| Ruby BUY | Quality-scored long signal with wave ratio and regime context |
| Ruby SELL | Quality-scored short signal with wave ratio and regime context |
| Regime Change | Market regime shift detected |
| Session Start / End | Trading session open and close |
| ORB Breakout Up / Down | 30-minute opening range breakout |
| IB Breakout Up / Down | 60-minute initial balance breakout |
| Squeeze Fired | Bollinger / Keltner squeeze expansion |

---

## Settings Overview

Ruby is fully configurable through grouped inputs:

| Group | What it controls |
|-------|-----------------|
| 📊 Dashboard Settings | Show/hide sections, position, theme |
| ⚡ Trend Speed Analysis | Asset type, EMA length, wave ratio, momentum |
| 🎨 Trend Speed Colors | Histogram colors |
| 🔍 Pattern Detection | S/R range, signal sensitivity |
| 📉 Sentiment: Trend & Momentum | AO periods, regime filter, multi-TF, momentum lookback |
| 🛡️ Support/Resistance | S/R lookback, sensitivity, higher-TF toggle |
| 🎨 Visual Settings | Colors, clean chart mode, entry zones, labels |
| ⏰ Time Settings | Start date, timer mode |
| 🕒 Session Settings | US / London / Asia / Custom hours, session filter |
| 🌡️ Volatility Settings | ATR, K-Means params, percentile thresholds |
| 🚨 Signal Settings | Quality threshold, cooldown, trend alignment, volume filter |
| 📍 Breakout Points | ORB, IB, Prev Day, Squeeze toggles and parameters |

---

## Quick Start

1. Add Ruby to your TradingView chart
2. Select your **Asset Type** (Gold, Crypto, Stocks, Forex) — this auto-tunes trend speed parameters
3. The dashboard appears in the top-right by default — toggle sections on/off as needed
4. Set up alerts for BUY, SELL, and breakout events
5. Use **Clean Chart Mode** if you want signals only without bands

---

## Recommended Timeframes

- **Scalping:** 1m – 5m (K-Means recalc set to 50+ recommended)
- **Intraday:** 5m – 15m (default settings work well)
- **Swing:** 1H – 4H (increase S/R lookback and regime MA length)

---

## License

[Mozilla Public License 2.0](https://mozilla.org/MPL/2.0/)

© nuniesmith 2026
