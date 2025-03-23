# CVD Divergence R-Multiple Backtest Enhanced

An enhanced version of the CVD (Cumulative Volume Delta) divergence strategy with comprehensive performance tracking and R-multiple based risk management.

## Overview

This enhanced version builds upon the original CVD divergence strategy by adding:

- Detailed profit tracking and balance management
- Maximum drawdown calculation
- Enhanced performance metrics
- Improved visualization with detailed performance tables
- Comprehensive trade statistics

## Features

### Core Strategy

- CVD (Cumulative Volume Delta) calculation
- Divergence detection between CVD and price
- R-multiple based risk management
- Maximum position hold time limit

### Performance Tracking

- Initial capital management (default: 10,000)
- Current balance tracking
- Maximum drawdown calculation
- Profit/Loss percentage tracking
- Win/Loss streak tracking
- Largest win/loss statistics

### Risk Management

- Configurable risk multiple (default: 1%)
- Configurable reward multiple (default: 2%)
- Maximum position hold time (default: 20 bars)
- Position size management (default: 100% of capital)

### Visualization

- Color-coded performance tables
- Signal markers on the chart
- Settings display
- Detailed statistics table including:
  - Signal type statistics
  - Win rates
  - R-multiple performance
  - Balance information
  - Drawdown metrics
  - P/L statistics

## Parameters

### Strategy Parameters

- `cvd_sma_length`: Length for CVD SMA (default: 50)
- `cvd_momentum_length`: Length for momentum calculation (default: 20)

### Risk Management

- `risk_multiple`: Risk per trade in percentage (default: 1.0%)
- `reward_multiple`: Reward target in percentage (default: 2.0%)
- `max_bars`: Maximum number of bars to hold a position (default: 20)

### Capital Management

- `initial_capital`: Starting capital (default: 10,000)
- `position_pct`: Position size as percentage of capital (default: 100%)

## Performance Metrics

### Trade Statistics

- Total trades (bullish/bearish)
- Success/failure counts
- Win rates
- R-multiple performance

### Financial Metrics

- Current balance
- Balance change percentage
- Maximum drawdown
- Largest win/loss percentages
- Win/loss streaks

## Usage

1. Apply the indicator to your chart
2. Adjust risk/reward parameters as needed
3. Monitor the performance table for:
   - Signal statistics
   - Balance information
   - Drawdown metrics
   - P/L statistics
4. Use the signal markers to identify entry points
5. Follow the R-multiple based risk management rules

## Best Practices

1. **Risk Management**

   - Start with conservative risk multiples
   - Monitor drawdown levels
   - Adjust position size based on account balance

2. **Signal Quality**

   - Look for strong divergences
   - Consider market context
   - Monitor volume confirmation

3. **Performance Monitoring**

   - Track win rates
   - Monitor R-multiple performance
   - Watch for drawdown levels

4. **Position Management**
   - Respect maximum hold time
   - Monitor profit targets
   - Follow stop loss levels

## Version History

### v1.0.0 (Initial Release)

- Added comprehensive profit tracking
- Implemented balance management
- Added maximum drawdown calculation
- Enhanced visualization with detailed performance tables
- Maintained original R-multiple functionality

## Notes

- The strategy is particularly effective on SOL
- Provides more signals compared to other implementations
- Enhanced version focuses on comprehensive performance tracking
- Original R-multiple functionality remains unchanged
