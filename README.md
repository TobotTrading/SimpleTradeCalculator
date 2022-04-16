# SimpleTradeCalculator
Basic single file HTML calculator for calculating trade size based on strict risk management with leverage support.

## Disclaimer
The code is published as is, without any warranty or support. I am not responsible for any loss or damage whatsoever, that may occur in connection with running or using this software. Use at your own risk.

Please note that this was a personal project that originally was not intended to be published or used in production. Nonetheless, I decided to share my work, so that others may profit. Generally my focus relied on functionality and a fast implementation, rather than code quality, performance, security, ... This project is not actively maintained, but I may push an update here and there if I feel like it.

## Usage
Open the file `SimpleTradeCalculator.html` in your favourite browser (tested on Chrome & Firefox).

![grafik](https://user-images.githubusercontent.com/99980186/163674403-070b474e-f54d-4bec-a537-bce21dbd1947.png)

The following fields need to be filled out accordingly:
- "Entry": Your entry price (float, >0)
- "Stop-Loss": Your stoploss price (float, >0)
- "Take-Profit": Your takeprofit price (float, >0)
- "Leverage": Leverage for your trade (int, >0, 1 = no leverage e.g. spot)
- "Type": Direction of trade (long, short)
- "Balance": Your trading account balance / maximum margin for a trade (float, >0)
- "Risk in %": Fixed risk depending on balance (float, >0)

The following conditions / edge cases are checked:
- "long": stoploss < entry < takeprofit
- "short": stoploss > entry > takeprofit
- "Leverage too high": Liquidation before stoploss (minimum margin / securities for your trading platform not taken into account)

## Dependencies
This project has no external dependencies.
