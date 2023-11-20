# GOLD Edge PRO MT5

This code is a sample implementation of the GOLD Edge PRO MT5 Forex robot developed by the Forex Robot Easy Team. The robot follows a trend-following strategy using moving averages and the RSI indicator. It places grid trades based on the calculated levels and closes orders when a drawdown occurs.

## Developer's site
For detailed reviews and trading results of this product, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/gold-edge-pro-mt5-review-trend-following-forex-ea/). Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample that can work as described in the product.

## Code Description
The code begins by including the necessary libraries and defining constants such as the trading symbol (SYMBOL), the distance between grid levels in pips (GRID_DISTANCE), and the trailing stop value in pips (TRAILING_STOP).

The code then initializes objects for trading (CTrade), calculating moving averages (CMovingAverages), and calculating the RSI (CRSI). It also initializes variables for storing the calculated values and the total number of orders.

The `CalculateIndicators()` function is used to calculate the moving averages and RSI values based on the current symbol and period.

The `PlaceGridTrades()` function is responsible for placing buy and sell orders at the calculated grid levels. It iterates over the total number of orders and calculates the grid level based on the current symbol's ask price and the grid distance.

The `CloseOrdersOnDrawdown()` function is used to close orders when a drawdown occurs. It closes the order with the specified ticket number and decreases the total number of orders by 2.

The `OnTick()` function is the main entry point and is executed on every tick. It first calculates the indicators and then checks if the fast moving average is greater than the slow moving average to determine the trend-following strategy.

If there are no open orders, it places the initial grid trades with the `PlaceGridTrades()` function and updates the total number of orders.

If the drawdown exceeds 5%, it closes the orders using the `CloseOrdersOnDrawdown()` function and decreases the total number of orders by 2.

## Product Description
GOLD Edge PRO MT5 is a trend-following Forex robot developed by the Forex Robot Easy Team. It utilizes moving averages and the RSI indicator to identify trends and place grid trades accordingly.

The robot is designed to trade the XAUUSD symbol and uses a grid trading strategy with a customizable grid distance between levels. It also incorporates a trailing stop to protect profits.

The trend-following strategy implemented in this robot aims to take advantage of market trends and generate profits in both upward and downward price movements.

Please note that this code is provided as a sample implementation of the GOLD Edge PRO MT5 Forex robot. For detailed reviews, trading results, and to find the official developer of this product, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/gold-edge-pro-mt5-review-trend-following-forex-ea/).
