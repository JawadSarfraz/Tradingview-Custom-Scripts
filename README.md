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
| **CVD with Order Blocks Basic**                     | Combines CVD analysis with Order Block detection for enhanced signal generation.                                                                    |
| **CVD-OB Multi-SMA Analysis**                       | Advanced version using multiple SMAs for refined signal generation and trend confirmation.                                                          |
| **CVD-OB Backtest Strategy**                        | Comprehensive backtesting implementation with detailed performance metrics and trade management.                                                    |

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

## CVD Divergence with EMA Trend Alignment

A streamlined version of the CVD divergence script that uses Exponential Moving Averages (EMAs) for trend alignment. This version focuses on taking trades in the direction of the prevailing trend.

### Features

- Uses 20 and 50 period EMAs for trend identification
- Takes bullish signals only in uptrends (EMA20 > EMA50)
- Takes bearish signals only in downtrends (EMA20 < EMA50)
- Implements R-multiple based backtesting (2R profit target, 1R stop loss)
- Tracks performance metrics including win rate and R-multiple returns
- Maximum trade duration of 20 bars before timeout

### Trading Rules

1. **Entry Conditions**:
   - Bullish: CVD divergence + EMA20 above EMA50
   - Bearish: CVD divergence + EMA20 below EMA50
2. **Trade Management**:
   - Enter on the next candle after signal
   - Take profit at 2R (twice the risk)
   - Stop loss at 1R (initial risk)
   - Trade expires after 20 bars if no target hit

### Performance Tracking

- Tracks total signals, successful trades, and win rates
- Calculates R-multiple returns for risk-adjusted performance
- Separate statistics for bullish and bearish signals
- Overall performance metrics including total R-multiple gained

### File Location

```
indicators/cvd/cvd_divergence_rmultiple_ema_backtest.pine
```

---

### **📊 CVD with Order Blocks Backtest Strategy**

🚀 **Advanced Backtesting System for CVD-OB Strategy**

### 🔹 **Features:**

- **Enhanced Performance Tracking:**

  - Total trades with win/loss statistics
  - Detailed profit/loss percentages
  - Largest win/loss tracking
  - Current and best/worst streaks
  - Maximum drawdown monitoring
  - Real-time balance updates

- **Position Management:**

  - Percentage-based position sizing
  - Dynamic stop-loss and take-profit levels
  - Maximum position hold time
  - Automated trade execution and exit

- **Signal Generation:**
  - CVD momentum analysis
  - Order Block detection with ATR filtering
  - Combined signal confirmation
  - Trend alignment checks

### 📈 **Parameters:**

- **Strategy Settings:**

  - Initial capital: 10,000 units
  - Position size: Configurable percentage
  - CVD Length: 20 periods (adjustable)

- **Risk Management:**
  - Take Profit: 2.0× risk (adjustable)
  - Stop Loss: 1.0× risk (adjustable)
  - Maximum hold time: 20 bars

### 🎯 **Performance Metrics:**

- **Trade Statistics:**

  - Total trades executed
  - Winning vs losing trades
  - Win rate percentage
  - Average win/loss size

- **Risk Metrics:**

  - Maximum drawdown
  - Best/worst trade
  - Winning/losing streaks
  - Current balance tracking

- **Visual Feedback:**
  - Entry/exit signals
  - Stop-loss/take-profit levels
  - Performance metrics table
  - Balance and drawdown tracking

✅ **Best Used With:**

- Multiple timeframe analysis
- Volume confirmation
- Market structure alignment
- Trend direction validation

---
