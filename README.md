# Pairs-Trading-Strategy-HDFCBANK-KOTAKBANK
This project demonstrates a quantitative approach to pairs trading using historical price data from HDFC and  and Kotak Mahindra Bank. Pairs trading is a market-neutral strategy that exploits the relationship between two stocks when they become temporarily mispriced. By using statistical tests and Python programming,this project explores the dynamics of these stocks, identifies trading signals, and backtests the strategy.

Motivation :

My interest in quantitative trading and financial markets drove me to explore pairs trading, a strategy well-suited for the volatile Indian stock market. This project allowed me to apply my skills in Python, statistics, and machine learning to real-world financial data.
Technologies Used :


Jupyter Notebook

Libraries: pandas, numpy, matplotlib, statsmodels, yfinance

Features :

Data Fetching: Automatically fetches historical stock data using the yfinance API. Exploratory Data Analysis: Includes cointegration tests and visualizations to understand the relationship between the stocks. Strategy Implementation: Implements the pairs trading strategy with clear, documented Python code. Backtesting: Backtests the strategy to evaluate its effectiveness and profitability over the past data.


Pair Trading Strategy (Simple Explanation)

Pair trading is a market-neutral strategy where you buy one asset and short-sell another related asset, typically in the same sector, to profit from the relative price movement between them. The idea is that both assets should move similarly, so if one goes up, the other should too (or vice versa). If there’s a price divergence between the two, you can exploit it by taking opposite positions.

How Pair Trading Works:

Identify Two Correlated Assets: Choose two assets that historically move in the same direction (e.g., two stocks in the same industry, two currencies, etc.).

Monitor Price Divergence: Wait for the price difference between the two assets to increase beyond the normal range. This creates an opportunity for profit if you believe the prices will revert to their historical relationship.

Take Positions:

Buy the undervalued asset.
Short the overvalued asset.
Profit When Prices Revert: When the prices of the two assets converge (move back toward their historical relationship), the long position (the asset you bought) gains value, and the short position (the asset you sold) loses value, but at a smaller rate. The net profit comes from this price correction.

Example: Pair Trading with Two Stocks
Suppose you are trading two stocks: Stock A and Stock B from the same industry, like Apple (AAPL) and Microsoft (MSFT).

Historically, these two stocks move in sync with a ratio of 1:1 (for every $1 increase in AAPL, MSFT also increases by $1).
Current prices:
AAPL = $150
MSFT = $160
If the ratio changes, for example, if MSFT moves up to $170 and AAPL stays at $150, the price difference has widened.

Current price difference: $170 (MSFT) - $150 (AAPL) = $20.
This is a larger than usual price gap, signaling an opportunity to trade.
Trading the Pair:
Sell MSFT (short position) at $170.
Buy AAPL (long position) at $150.
Profit Scenario:
If the stocks revert to their historical price relationship, say MSFT drops to $160 and AAPL rises to $155, the prices converge.
Long AAPL position gains $5 (from $150 to $155).
Short MSFT position gains $10 (from $170 to $160).
Total profit = $5 (AAPL gain) + $10 (MSFT gain) = $15.
Key Points:
Market-neutral: It doesn't rely on the direction of the overall market, only the relative price movement between the two assets.
Risk is lower: You hedge the overall market risk, as the two assets are correlated.
Requires monitoring: The strategy depends on tracking and predicting the relationship between the two assets.
