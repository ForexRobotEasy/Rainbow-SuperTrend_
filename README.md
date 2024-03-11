# Rainbow SuperTrend

Rainbow SuperTrend is a custom indicator developed by the Forex Robot Easy Team. It enhances trading on the MetaTrader 5 (MT5) platform by providing trend direction and stop loss levels based on the Average True Range (ATR) model.

## Indicator Initialization

The indicator is initialized in the `OnInit()` function. It sets up the indicator buffers and labels, as well as the indicator style. There are two indicator buffers used: `rainbowSuperTrendBuffer` and `stopLossBuffer`. Both buffers are set to be displayed as lines on the chart.

## Indicator Calculation

The `OnCalculate()` function is responsible for calculating the Rainbow SuperTrend and stop loss levels for each bar on the chart. It iterates through the bars from the last calculated bar (`prev_calculated`) to the current bar (`rates_total`). For each bar, it calls the `CalculateRainbowSuperTrend()` and `CalculateStopLoss()` functions to calculate the respective values and stores them in the indicator buffers.

## Calculate Rainbow SuperTrend

The `CalculateRainbowSuperTrend()` function calculates the Rainbow SuperTrend value for a given bar index. It first calculates the Average True Range (ATR) using the built-in `iATR()` function. Then, it determines the trend direction based on whether the current bar's closing price is higher or lower than the previous bar's closing price. The trend direction is then adjusted based on the ATR value. Finally, the Rainbow SuperTrend value is calculated by adding the ATR multiplied by the trend direction to the previous bar's closing price.

## Calculate Stop Loss

The `CalculateStopLoss()` function suggests stop loss levels based on the Rainbow SuperTrend line. If the current Rainbow SuperTrend value is higher than the previous value, the stop loss is set to the previous value. If the current Rainbow SuperTrend value is lower than the previous value, the stop loss is also set to the previous value. If the current and previous Rainbow SuperTrend values are the same, the stop loss is set to the current value.

For detailed reviews and trading results of this product, visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/rainbow-supertrend-review-enhance-mt4-trading-with-atr-based-trends/). Please note that Forex Robot Easy is not the official developer of this product. This code serves as a sample that can work as described in the product. To find the official developer of this product, please use MQL5.
