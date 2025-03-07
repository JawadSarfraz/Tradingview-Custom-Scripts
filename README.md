# TradingView-Custom-Scripts

A collection of custom TradingView Pine Scripts for technical analysis, market insights, and automated trading signals.

## 📂 Scripts Included

| Script Name                                         | Description                                                                                                                                         |
| --------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **CVD-Based Divergences (SMA 50)**                  | Detects **bullish & bearish divergences** using CVD vs. price action, now optimized with **SMA 50** for stronger trend filtering.                   |
| **CVD-Based Divergences with Momentum Strength**    | Enhances CVD divergences by measuring **weak, medium, and strong divergences** using **momentum strength**. **Only strong signals trigger alerts.** |
| **CVD Divergences with Momentum Strength - Logger** | Advanced version that tracks and analyzes signal performance with historical success rates and detailed statistics.                                 |
| **CVD Divergences Backtest**                        | Specialized version for backtesting divergence signals with comprehensive performance metrics and profit analysis.                                  |
| **CVD Divergences R-Multiple Backtest (RSI)**       | Enhanced backtest version incorporating RSI confirmation for improved signal quality and performance tracking.                                      |
| **Filtered Bullish Fair Value Gaps**                | Highlights strong **FVG zones** to spot potential trade setups.                                                                                     |
| **Bullish Order Block Finder (V1)**                 | Detects **Bullish Order Blocks** with volume confirmation.                                                                                          |

---

### **📊 CVD-Based Divergences with Momentum Strength - Logger**

🚀 **Performance Tracking System for CVD Divergence Signals**

### 🔹 **Features:**

- **Signal Strength Classification:**

  - Strong signals: CVD & Price strength > 1.2
  - Medium signals: CVD & Price strength > 1.0
  - Weak signals: CVD & Price strength < 1.0

- **Real-time Performance Metrics:**

  - Overall success rate
  - Recent performance (last 10 signals)
  - Total historical signals count

- **Signal Validation:**

  - Tracks next candle movement for success/failure
  - Separate tracking for bullish and bearish signals
  - Historical performance logging

- **Debug Information:**
  - Current CVD and Price strength values
  - Divergence conditions status
  - Real-time signal strength monitoring

### 📈 **Parameters:**

- **SMA Periods:**

  - CVD SMA: 50 periods
  - Momentum Length: 20 periods
  - Price Momentum: 20 periods

- **Strength Thresholds:**
  - Strong Signal: > 1.2
  - Medium Signal: > 1.0
  - Weak Signal: < 1.0

✅ **Best Used With:**

- **Multiple Timeframe Analysis**
- **Volume Confirmation**
- **Support & Resistance Zones**
- **Trend Direction Validation**

---

### **📊 CVD-Based Divergences (SMA 50)**

🚀 **Smart Money Cumulative Volume Delta (CVD) Divergence Detector**

### 🔹 **Features:**

- Uses **SMA 50** for trend filtering to **reduce noise & false signals**.
- Identifies **bullish divergences** when **CVD rises but price falls** (Accumulation).
- Detects **bearish divergences** when **CVD falls but price rises** (Distribution).
- Best suited for **swing trading & long-term trend analysis** (1H, 4H, 1D, 1W timeframes).

### 📈 **How It Works:**

1. **Bullish Divergence (Buy Signal)**:

   - **CVD increasing** (more buying pressure).
   - **Price decreasing** (weak selling).
   - Smart money is **accumulating** → Potential price increase.

2. **Bearish Divergence (Sell Signal)**:
   - **CVD decreasing** (more selling pressure).
   - **Price increasing** (fake breakout).
   - Smart money is **distributing** → Potential price drop.

✅ **Best Used With**:

- **Order Blocks (OBs)**
- **Fair Value Gaps (FVGs)**
- **Support & Resistance Zones**
- **EMA 50/200 for trend confirmation**

---

### ** CVD-Based Divergences with Momentum Strength**

**Advanced Smart Money Divergence Detection**

### 🔹 **New Features:**

- **Measures divergence strength** → **Weak, Medium, and Strong** divergences.
- **Filters out weak signals** → Only strong divergences trigger alerts.
- **Color-coded visualization**:
  - 🟢 **Strong Bullish** = **High confidence reversal up**
  - 🟡 **Medium Bullish** = **Moderate confidence**
  - ⚪ **Weak Bullish** = **Unreliable, avoid**
  - 🔴 **Strong Bearish** = **High confidence reversal down**
  - 🟠 **Medium Bearish** = **Moderate confidence**
  - ⚪ **Weak Bearish** = **Unreliable, avoid**
- **Best for short-term & swing traders looking for high-confidence reversals.**

### 📈 **How It Works:**

1. **Divergence Strength Calculation**:
   - **Compares CVD & price momentum** to their historical averages.
   - **Normalizes movement** so only significant divergences matter.
2. **Strong Divergences (Best for Trading)**:
   - **CVD Momentum Strength > 1.5**
   - **Price Momentum Strength > 1.5**
   - ✅ **Higher probability of reversal!**
3. **Weak Divergences (Ignore These)**:
   - **CVD Momentum Strength < 1**
   - **Price Momentum Strength < 1**
   - ❌ **Not enough confirmation for a trade!**
     ✅ **Best Used With**:

- **Order Blocks (OBs)**
- **Fair Value Gaps (FVGs)**
- **High Volume Confirmation**
- **Multi-Timeframe Analysis**

---

### **📊 CVD Divergences Backtest**

🚀 **Comprehensive Backtesting System for CVD Divergence Signals**

### 🔹 **Features:**

- **Signal Performance Tracking:**

  - Separate tracking for bullish and bearish signals
  - Success rate calculation for each signal type
  - Overall performance statistics

- **Performance Metrics:**

  - Total signals generated
  - Success count by signal type
  - Success rate percentages
  - Total profit calculation
  - Maximum drawdown tracking
  - Profit factor analysis

- **Visual Analytics:**
  - Real-time statistics table
  - Performance metrics display
  - Signal markers on chart
  - Profit/drawdown visualization

### 📈 **Parameters:**

- **SMA Settings:**

  - CVD SMA Length: 50 periods
  - Momentum Length: 20 periods

- **Profit Calculation:**
  - Default 1% profit target per trade
  - Adjustable profit targets
  - Drawdown tracking

✅ **Best Used For:**

- Analyzing historical performance
- Optimizing strategy parameters
- Risk assessment
- Performance comparison across timeframes

---

### **📊 CVD Divergences R-Multiple Backtest (RSI)**

🚀 **Advanced Backtest System with RSI Confirmation**

### 🔹 **Features:**

- **RSI Integration:**

  - Uses RSI(14) for signal confirmation
  - Oversold level at 40 for bullish signals
  - Overbought level at 60 for bearish signals
  - Visual RSI level indicators

- **Signal Requirements:**

  - Bullish: CVD divergence + RSI oversold condition
  - Bearish: CVD divergence + RSI overbought condition
  - Automated signal validation

- **Performance Metrics:**
  - Total signals with RSI confirmation
  - Success rate for RSI-confirmed signals
  - R-multiple calculation for risk-adjusted returns
  - Separate tracking for timeouts

### 📈 **Parameters:**

- **RSI Settings:**

  - Length: 14 periods
  - Oversold: 40 (more aggressive than traditional 30)
  - Overbought: 60 (more aggressive than traditional 70)

- **Risk Management:**
  - Configurable R-multiple targets
  - Default 2R profit target
  - 1R stop loss
  - Maximum 20 bars hold time

### 🎯 **Signal Logic:**

1. **Bullish Signal Requirements:**

   - CVD increasing while price decreasing
   - RSI below 40 (oversold)
   - No active trade in progress

2. **Bearish Signal Requirements:**
   - CVD decreasing while price increasing
   - RSI above 60 (overbought)
   - No active trade in progress

✅ **Best Used For:**

- Trend reversal confirmation
- Momentum-based entries
- Risk-managed position taking
- Performance analysis and optimization

---
