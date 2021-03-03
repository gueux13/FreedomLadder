# Implementation on IBKR

## Roadmap:

0. Speedroll:

      (i) understand the kind of data that can be requested from the server.
      (ii) understand the order types, atomic trading actions can be sent to the server
      (iii) glue conditions on market data and trading strategies together to form a gap-and-go for proof of concept.

1. Alpha test the trading bot on the paper trading account.

## Code components:

A scanner class:

      purpose: find possible setup for trading strategies across the market.
      
      basic functions: acquire non-realtime market data in interval of seasonal earnings, days, at close, occasionally the current price across the whole market.
                       basic filtering functions on these data (>, <, range, ratios).
                       
      possible difficulties: acquire and quantify news catalysts.

A trader class:

      purpose: calculate realtime or recent technical indicators to produce buy and sell signal for a single stock.
      
      basic functions: acquire and store realtime market data, calculate techincal indicators
