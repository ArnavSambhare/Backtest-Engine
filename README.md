# Backtest-Engine

This contains the engine to backtest trading strategies.
It contains two classes (Stock and Portfolio). 

Stock Class needs to be initialized by passing a dataframe(downloaded from yahoo finance website, needs to be in the same format) and a string ticker symbol.
Then signals must be added to the stock if the dataframe passed doesn't contain a column named 'Signals'.
This class contains:
1. plot_returns_distribution which plots the daily returns of the stock on a histogram.
2. plot_daily_volatility which plots the daily price volatility of the stock.
3. plot_prices which plots the daily closing prices.
4. add_signals which adds the signals to the Stock.


Portfolio class needs to be initialized by passing the initial cash, a date for when the portfolio is created.
This class contains:
1. cash_available: returns the cash(liquid) available at hand at the moment
2. add_stocks: pass a list containing the stocks (Stock classes) to be added into the portfolio.
3. cumulative_return: after passing a date, this returns the net return till this date.
4. show_positions: this returns the current position of the portfolio
5. backtest: end date and start date(in the same order) must be passed. This runs the backtest and       prints the cash, return and maximum drawdown.
6. plot_cash: This plots the daily liquid cash at hand during the backtest.
7. plot_valuation: This plots the daily value of the total cash.
8. view_transaction_logs: This returns a list of the all the transactions that took place and their corresponding dates.
