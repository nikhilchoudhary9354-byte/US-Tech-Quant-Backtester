# US Tech Quant Backtester

A Python-based backtesting engine that tests a Moving Average Crossover trading strategy on 5 major US tech stocks: **AAPL, NVDA, GOOGL, AMZN, and TSLA**.

## What it does

- Downloads historical price data using `yfinance`
- Generates buy/hold signals using a 20-day and 50-day Moving Average crossover
- Simulates a $100,000 portfolio split equally across the 5 stocks
- Applies a 0.1% transaction cost on every trade
- Calculates performance metrics for each stock:
  - Final portfolio value and return %
  - Win rate (per trade)
  - Sharpe Ratio (risk-free rate assumed to be 0%)
  - Max Drawdown
- Plots the equity curve for each stock and the combined portfolio

## How to run

1. Clone this repo
2. Install the required libraries:
   ```
   pip install -r requirements.txt
   ```
3. Run the notebook (`US-Tech-Quant-Backtester.ipynb`) in Jupyter or Google Colab, or run the script directly:
   ```
   python US-Tech-Quant-Backtester.py
   ```

## Sample Output

```
Stock: NVDA
 -> Final Value: $32888.11 | Return: 64.44% | Win Rate: 80.0% (5 trades)
 -> Sharpe Ratio: 1.65 | Max Drawdown: -12.12%
```

## A note on Win Rate

Win rate is calculated per trade (not per day). Since this strategy only makes a small number of trades (usually under 10 per stock over 2 years), win rate percentages can look extreme just due to small sample size, so they should be read with some caution rather than taken as a guarantee the strategy works well in general.

## Tech Used

Python, Pandas, NumPy, Matplotlib, yfinance

## Author

Nikhil Choudhary
[LinkedIn](https://linkedin.com/in/nikhilchoudhary) | [GitHub](https://github.com/nikhilchoudhary9354-byte)
