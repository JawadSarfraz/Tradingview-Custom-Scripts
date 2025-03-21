# CVD with Order Blocks Backtesting

A comprehensive backtesting implementation for the CVD-OB (Cumulative Volume Delta with Order Blocks) strategy, now featuring multiple SMA analysis for enhanced signal quality.

## Strategy Overview

This backtesting script implements a systematic trading approach combining CVD momentum with Order Block detection, using multiple SMAs for better trend confirmation and signal classification.

### Core Components

1. **Signal Generation**

   - Triple SMA system for CVD analysis
   - Dual SMA system for price trend confirmation
   - Order Block confirmation with ATR filtering
   - Signal strength classification (Strong/Medium)

2. **Risk Management**

   - Percentage-based position sizing
   - Dynamic stop-loss and take-profit levels
   - Maximum position hold time
   - Automated trade management

3. **Performance Analytics**
   - Real-time performance tracking
   - Color-coded metrics visualization
   - Trade statistics and balance monitoring
   - Risk-adjusted returns calculation

### Parameters

| Category        | Parameter     | Default | Description                   |
| --------------- | ------------- | ------- | ----------------------------- |
| CVD SMAs        | Fast          | 10      | Quick momentum detection      |
|                 | Medium        | 21      | Intermediate trend            |
|                 | Slow          | 50      | Long-term trend               |
| Price SMAs      | Fast          | 10      | Short-term price trend        |
|                 | Slow          | 21      | Medium-term price trend       |
| Risk Management | Take Profit   | 2.0     | Multiple of risk              |
|                 | Stop Loss     | 1.0     | Risk percentage               |
|                 | Max Hold Bars | 20      | Maximum trade duration        |
| Order Blocks    | ATR Length    | 14      | Volatility measurement period |
|                 | OB Threshold  | 1.2     | Minimum candle size (× ATR)   |

## Signal Classification

### 1. Strong Signals

- Requirements:
  - All three CVD SMAs aligned (Fast, Medium, Slow)
  - Price trend confirmation (Fast > Slow SMA)
  - Valid Order Block formation
- Visual: Large triangles (green/red)

### 2. Medium Signals

- Requirements:
  - Two CVD SMAs aligned (Fast and Medium)
  - Price trend confirmation
  - Valid Order Block formation
- Visual: Small triangles (green/red)

## Performance Metrics Display

The strategy features an enhanced visual performance metrics table:

### 1. Table Layout

- **Header Row** (Light Blue Background)

  - Performance Metrics | Value | Percentage

- **Trade Statistics** (Color-Coded)
  - Total Trades (Light Blue)
  - Winning Trades (Light Green)
  - Losing Trades (Light Red)
  - Current Balance (Light Gold)

### 2. Color Scheme

- Headers: Light Blue (#66B2FF, 20% transparency)
- Total Trades: Blue (#2962FF, 90% transparency)
- Winning Trades: Green (#00C853, 90% transparency)
- Losing Trades: Red (#FF1744, 90% transparency)
- Balance Info: Gold (#FFB300, 90% transparency)
- Text: Black for maximum readability

## Implementation Notes

### 1. Signal Generation Logic

```pine
// Strong signals require alignment of all SMAs
strong_bullish = cvd_fast_momentum > 0 and
                 cvd_medium_momentum > 0 and
                 cvd_slow_momentum > 0 and
                 uptrend

// Medium signals require alignment of fast and medium SMAs
medium_bullish = cvd_fast_momentum > 0 and
                 cvd_medium_momentum > 0 and
                 uptrend
```

### 2. Trade Management

- Entry on signal confirmation
- Exit on:
  - Stop loss hit
  - Take profit reached
  - Maximum hold time exceeded

### 3. Visual Feedback

- Price SMAs plotted on chart
- Signal triangles sized by strength
- Stop loss and take profit levels shown
- Real-time performance metrics

## Best Practices

1. **Timeframe Selection**

   - Higher timeframes: More reliable signals
   - Lower timeframes: More opportunities
   - Recommended: 1H or higher

2. **Signal Interpretation**

   - Strong signals: Higher probability setups
   - Medium signals: Require additional confirmation
   - Consider overall market context

3. **Risk Management**
   - Use appropriate position sizing
   - Honor stop losses
   - Monitor maximum drawdown
   - Track performance metrics

## Version History

### Latest Version (3.0)

- Implemented triple SMA system for CVD
- Added signal strength classification
- Enhanced visual feedback system
- Improved performance metrics display

### Previous Version (2.1)

- Enhanced performance metrics visualization
- Improved color scheme for readability
- Added real-time balance tracking
- Optimized table layout and formatting

### Initial Version (2.0)

- Basic CVD-OB implementation
- Simple trade tracking
- Basic performance metrics
- Manual position sizing
