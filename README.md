# Filtered MACD spot trading strategy

Trades on MACD crossover signals, using RSI, EMA, ATR, and crossover angles as filters.

## Filters

### MACD crossover angle

The difference between the gradients of the MACD and signal lines are used as a filter. 

If the angle is too shallow, then the trade is avoided. 

Crossovers are marked on the indicator with green and red crosses.

| Parameter | Description |
|---|---|
| Fast length | Fast MA length |
| Slow length | Slow MA length |
| Signal length | MACD signal length |
| Buy MACD angle | Minimum MACD crossover angle for buying (not normalised, will need calibrating for each pair) |
| Sell MACD angle | Minimum MACD crossover angle for selling (not normalised, will need calibrating for each pair) |


#### RSI cutoff 

If the RSI is too high, i.e. approaching overbought the buy trade is avoided.

Blue background => RSI high, don't trade

| Parameter | Description |
|---|---|
| RSI length | RSI length |
| Cutoff | Trades are avoided when RSI is above this value |


### EMA uptrend

Trades are only made when the market is in uptrend. A parameter is used to look back N candles to see if the price is moving up or down.

Red background => downtrend

Green background => uptrend

| Parameter | Description |
|---|---|
| EMA length | EMA length |
| EMA uptrend length | Number of candles to look back to determine if market is in uptrend |

### ATR cutoff
If the ATR is too low, i.e. the market is not moving with much momentum, avoid making trades.

ATR is a non-normalised indicator so will need to be adjusted for each trading pair.

Purple background => ATR low, don't trade

| Parameter | Description |
|---|---|
| ATR length | ATR length |
| Cutoff | Trades are avoided when ATR is below this value |
