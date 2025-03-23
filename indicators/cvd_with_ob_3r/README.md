# CVD-OB 3R Backtest Strategy

This is an enhanced version of the CVD-OB (Cumulative Volume Delta with Order Blocks) strategy that implements a 3:1 risk-reward ratio for improved risk management.

## Key Features

- **3:1 Risk-Reward Ratio**: Optimized for better risk management with wider take-profit targets
- **Multi-SMA System**: Uses three SMAs for CVD and two SMAs for price to identify trends
- **Order Block Detection**: Identifies significant price levels for entry and exit
- **Performance Tracking**: Comprehensive metrics including win rate, profit/loss tracking, and drawdown monitoring
- **Visual Feedback**: Clear entry/exit signals and performance metrics display

## Strategy Components

### 1. CVD (Cumulative Volume Delta) Analysis

- Fast SMA (10 periods)
- Medium SMA (21 periods)
- Slow SMA (50 periods)
- Momentum calculation using multiple timeframes

### 2. Price Analysis

- Fast SMA (10 periods)
- Slow SMA (21 periods)
- Trend identification using SMA crossovers

### 3. Order Block Detection

- Uses ATR for volatility-based significance
- Identifies strong bullish and bearish candles
- Confirms with subsequent price action

### 4. Risk Management

- 3:1 Risk-Reward ratio (configurable)
- Stop Loss: 1% (default)
- Take Profit: 3% (default)
- Maximum position hold time: 20 bars (configurable)

## Signal Generation

### Strong Signals

- All three CVD SMAs aligned
- Price trend confirmation
- Valid Order Block present

### Medium Signals

- Fast and medium CVD SMAs aligned
- Price trend confirmation
- Valid Order Block present

## Performance Metrics

The strategy tracks and displays:

- Total number of trades
- Win rate percentage
- Loss rate percentage
- Current balance and performance
- Maximum drawdown
- Win/loss streaks

## Usage

1. Apply the indicator to your chart
2. Configure the risk management parameters:
   - Take Profit Multiple (default: 3.0)
   - Stop Loss Multiple (default: 1.0)
   - Maximum Position Hold Bars (default: 20)
3. Adjust SMA periods if needed
4. Monitor the performance metrics table

## Best Practices

1. **Timeframe Selection**:

   - Recommended for 1H and 4H timeframes
   - Higher timeframes may require parameter adjustment

2. **Risk Management**:

   - Maintain the 3:1 ratio for optimal risk-reward
   - Adjust position size based on account size
   - Monitor maximum drawdown

3. **Market Conditions**:
   - Best performance in trending markets
   - Reduced signals in ranging markets
   - Consider market volatility when setting parameters

## Version History

### v1.0 (Initial Release)

- Implemented 3:1 risk-reward ratio
- Added multi-SMA system
- Enhanced performance tracking
- Improved visual feedback
