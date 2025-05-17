Bybit Past Funding rate download link: https://www.bybit.com/en/announcement-info/fund-rate/ 
Binance Past Funding rate download link: https://www.binance.com/en/futures/funding-history/quarterly/funding-fee-history

Each period is 8 hours;
Starting with an initial capital of 1,000,000 USDT (non-compounding).

Entry Logic:

If the BTC spot Close price remains above the daily MA120 (calculated from BTC spot prices) for 9 consecutive 8-hour periods (3 days), 
then from the 10th period onward, monitor whether the funding rate turns positive. 
If the funding rate becomes positive at the end of the (10+n)th period, then at the beginning of the (11+n)th period, 
place a limit order to buy BTC spot at the spot opening price, and immediately transfer the BTC to the BTC token margined perpetual futures account, 
placing a limit order to short 1x leverage futures at the same price, using the entire spot position size. (n = 0, 1, 2, 3, ….) 

(For example, if the funding rate becomes positive at the end of the 13th period, then execute the spot buy and futures short at the opening price of the 14th period.)

Exit Logic: 
Similarly, if the BTC spot Close price stays below the daily MA120 for 9 consecutive 8-hour periods, 
then starting from the 10th period, monitor whether the funding rate turns negative. 
If the funding rate becomes negative at the end of the (10+n)th period, then at the beginning of the (11+n)th period, 
place a limit order to buy futures to close the short position at the futures opening price, 
and immediately transfer all BTC back to the spot account and place a limit sell order at the same price to exit the BTC spot position.
