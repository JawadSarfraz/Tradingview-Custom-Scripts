# CVD with Order Blocks Backtesting

A comprehensive backtesting implementation for the CVD-OB (Cumulative Volume Delta with Order Blocks) strategy.

## Strategy Overview

This backtesting script implements a systematic trading approach combining CVD momentum with Order Block detection, featuring enhanced performance metrics and trade management.

### Core Components

1. **Signal Generation**

   - CVD momentum analysis (above/below SMA)
   - Order Block confirmation with ATR filtering
   - Combined momentum and structure analysis
   - Trend alignment validation

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

| Parameter       | Default | Description                       |
| --------------- | ------- | --------------------------------- |
| Initial Capital | 10000   | Starting trading capital          |
| Position Size % | 100     | Percentage of capital per trade   |
| CVD Length      | 20      | Period for CVD SMA calculation    |
| TP Multiple     | 2.0     | Take profit as multiple of risk   |
| SL Multiple     | 1.0     | Stop loss as multiple of risk     |
| Max Hold Bars   | 20      | Maximum bars to hold position     |
| ATR Length      | 14      | ATR period for volatility measure |
| OB Threshold    | 1.2     | Order Block ATR multiplier        |

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

### 3. Metrics Displayed

- Trade counts and percentages
- Win/loss ratios
- Current balance and change
- Real-time performance updates

## Usage Guide

1. **Setup**

   - Apply to any instrument with volume data
   - Recommended timeframe: 1H or higher
   - Configure initial capital and position size
   - Adjust risk parameters based on strategy

2. **Parameter Optimization**

   - Fine-tune CVD length for market conditions
   - Adjust R:R ratio based on win rate
   - Optimize hold time for trade duration
   - Calibrate ATR multiplier for volatility

3. **Performance Analysis**
   - Monitor color-coded metrics table
   - Track win rate and balance changes
   - Analyze trade patterns
   - Evaluate strategy effectiveness

## Future Improvements

1. **Short Term**

   - Enhanced trade logging functionality
   - Additional performance metrics
   - Time-based trade filtering
   - Volume profile integration

2. **Long Term**
   - Multi-timeframe analysis
   - Dynamic position sizing
   - Market regime detection
   - Machine learning signal filtering

## Implementation Notes

- Uses percentage-based position sizing for consistent risk
- Implements automatic trade management with R-multiple targets
- Tracks comprehensive performance metrics in real-time
- Provides clear visual feedback through color-coded display

## Best Practices

1. **Trade Management**

   - Use appropriate position sizing
   - Monitor drawdown levels
   - Follow stop-loss discipline
   - Track performance regularly

2. **Risk Control**
   - Never override stop-losses
   - Maintain consistent position sizes
   - Monitor cumulative risk
   - Track correlation with market

## Contributing

Areas for contribution:

1. Parameter optimization research
2. Additional performance metrics
3. Enhanced risk management features
4. Market regime detection
5. Multi-timeframe analysis integration

## Version History

### Latest Version (2.1)

- Enhanced performance metrics visualization
- Improved color scheme for better readability
- Added real-time balance tracking
- Optimized table layout and formatting

### Previous Version (2.0)

- Added enhanced performance metrics
- Implemented percentage-based position sizing
- Added comprehensive trade tracking
- Improved visual feedback system

### Initial Version (1.0)

- Basic CVD-OB implementation
- Simple trade tracking
- Basic performance metrics
- Manual position sizing
