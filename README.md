# 🕯️ BAKOME Candles V3 – Institutional Strength & Optimization Engine for MT5

## Trend Strength · EMA Crossover · ATR‑Based SL/TP · Non‑Repainting Arrows

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![MQL5](https://img.shields.io/badge/MQL5-Indicator-005F99)](https://www.mql5.com)
[![Platform](https://img.shields.io/badge/Platform-MT5-blue)](https://www.metatrader5.com)

---

## 🔥 Features

| Feature | Description |
|---------|-------------|
| **Strength Engine** | Calculates proprietary strength value based on momentum and trend (EMA 20/100) |
| **EMA Trend Crossover** | Fast (20) and slow (100) EMA – clear buy/sell conditions |
| **ATR‑based SL/TP** | Dynamic stop loss and take profit levels based on current volatility |
| **Market State Detection** | Bull/Bear strength levels (Strong/Med/Light) + Neutral |
| **Non‑Repainting Arrows** | Buy (green) and Sell (red) arrows on closed bars – no repainting |
| **Alert System** | Popup and push notifications – one alert per signal (no spam) |
| **Dashboard** | Real‑time display of market state, ATR, and signal counters |
| **Lightweight & Fast** | Optimised indicator handles, no memory leaks |

---

## 🛠️ Installation

1. **Download** `BAKOME_Candles_V3.mq5` from this repository.
2. **Place** the file in `MQL5/Indicators/` folder.
3. **Compile** (F7) in MetaEditor.
4. **Attach** to any chart (any timeframe – M5 recommended).
5. Adjust input parameters according to your trading style.

---

## ⚙️ Input Parameters

| Parameter | Default | Description |
|-----------|---------|-------------|
| `StrengthPeriod` | 8 | Period for strength calculation (reserved for future use) |
| `ATRPeriod` | 14 | Period for ATR calculation |
| `FastEMA` | 20 | Fast EMA period |
| `SlowEMA` | 100 | Slow EMA period |
| `EnableAlerts` | true | Enable popup alerts |
| `EnablePush` | true | Enable push notifications |
| `EnableArrows` | true | Show buy/sell arrows on chart |
| `ATR_SL_Multiplier` | 1.5 | Stop loss distance in ATR units |
| `ATR_TP_Multiplier` | 3.0 | Take profit distance in ATR units |
| `BullColor` | clrLime | Colour for buy arrows and bullish strength line |
| `BearColor` | clrTomato | Colour for sell arrows and bearish strength line |

---

## 📊 How It Works

1. The indicator calculates **EMA20** and **EMA100** using cached handles.
2. **Strength** is computed as `0.6 * (Close - EMA20) + 0.4 * (EMA20 - EMA100)`.
3. **Market state** is determined from the strength value:
   - `> 100` → BULL STRONG
   - `50–100` → BULL MED
   - `0–50` → BULL LIGHT
   - `0 to -50` → BEAR LIGHT
   - `-50 to -100` → BEAR MED
   - `< -100` → BEAR STRONG
4. A **BUY signal** appears when: `Close > Fast EMA > Slow EMA`.
5. A **SELL signal** appears when: `Close < Fast EMA < Slow EMA`.
6. When a signal is generated on the **closed bar**, an arrow is plotted, and an alert is sent (once per bar).
7. ATR‑based stop loss and take profit levels are calculated and drawn as horizontal lines on the chart.
8. The dashboard shows current state, ATR value, and total signal counts.

---

## 💡 Tips

- Combine with support/resistance zones for higher accuracy.
- Use on M5 for scalping or on higher timeframes for swing trading.
- Test thoroughly on a demo account before live trading.

---

## 💰 Crypto Donations (Support Open Source)

If this indicator helps you trade, consider supporting its development:

| Network | Address |
|---------|---------|
| **Bitcoin (BTC)** | `bc1qhtjp3qpqru4vuqd355dfcn46mqjrlpdfmngk6u0` |
| **Ethereum (ETH)** | `0x2fD73626714d9e37EA464109F8eCeA2CA5401062` |
| **Solana (SOL)** | `3CfhghA7hSNPBbd1RME5rRDm5UUeesTq9NKTcyzZdkz4` |
| **USDT (TRC20)** | `THkLdiKsmscJFwBPA4tpWeAn1xVw7DTKxq` |

👉 [Sponsor on Drips](https://app.drips.network/projects/BAKOME-Hub/BAKOME_Candles_V3)

---

## 📜 License

**MIT** – free for personal and commercial use. No hidden fees.

---

## 👑 Author

**Bakome Fabrice Kitoko** – Goma, Democratic Republic of Congo 🇨🇩  
[GitHub](https://github.com/BAKOME-Hub) | [Email](mailto:fabienbakome@gmail.com)

---

<p align="center">
  <img src="https://img.shields.io/badge/Trend-Strength-00FF88?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Advanced-Indicator-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Open%20Source-MIT-green?style=for-the-badge"/>
</p>
