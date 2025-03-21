# CVD with Order Blocks Backtesting

A comprehensive backtesting implementation for the CVD-OB (Cumulative Volume Delta with Order Blocks) strategy.

## Strategy Overview

This backtesting script implements a systematic trading approach combining CVD momentum with Order Block detection.

### Core Components

1. **Signal Generation**

   - CVD above/below SMA(20)
   - Order Block confirmation
   - Combined momentum and structure analysis

2. **Risk Management**
   - Dynamic position sizing based on ATR
   - Configurable risk:reward ratios
   - Maximum position hold time
   - Automatic stop-loss and take-profit levels

### Parameters

| Parameter     | Default | Description                     |
| ------------- | ------- | ------------------------------- |
| CVD Length    | 20      | Period for CVD SMA calculation  |
| TP Multiple   | 2.0     | Take profit as multiple of risk |
| SL Multiple   | 1.0     | Stop loss as multiple of risk   |
| Max Hold Bars | 20      | Maximum bars to hold position   |

## Performance Metrics

The strategy tracks several key performance indicators:

1. **Trade Statistics**

   - Total number of trades
   - Win rate percentage
   - Maximum drawdown

2. **Visual Feedback**
   - Entry signals (triangles)
   - Stop loss levels (red lines)
   - Take profit levels (green lines)
   - Performance metrics table

## Usage Guide

1. **Setup**

   - Apply to any instrument with volume data
   - Recommended timeframe: 1H or higher
   - Initial capital: 10,000 units
   - Position size: 100% of equity

2. **Parameter Optimization**

   - Adjust CVD length based on market volatility
   - Modify R:R ratio based on market conditions
   - Fine-tune max hold time based on average trend duration

3. **Performance Analysis**
   - Monitor win rate for strategy effectiveness
   - Track drawdown for risk assessment
   - Analyze trade duration distribution

## Future Improvements

1. **Short Term**

   - Add trade logging functionality
   - Include more performance metrics
   - Implement trade filtering based on time

2. **Long Term**
   - Add multi-timeframe analysis
   - Implement dynamic position sizing
   - Add market regime detection
   - Include volatility-based parameter adjustment

## Notes

- The strategy uses percentage-based position sizing
- All exits are managed with automatic stop-loss and take-profit orders
- Maximum drawdown calculation uses peak-to-trough methodology
- Performance metrics are updated in real-time

## Contributing

Feel free to suggest improvements or report issues. Key areas for contribution:

1. Parameter optimization
2. Additional performance metrics
3. Enhanced risk management features
4. Market regime detection
