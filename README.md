# Apple Inc. (AAPL): Historical Analysis

## 1. AAPL Historical Price and Performance Analysis

### Project overview

This project examines Apple Inc. (AAPL) daily historical prices from January 2, 2020, to November 17, 2026. Using Python, pandas, and Matplotlib, it explores the performance, adjusted-price movements and daily returns. The goal is to describe AAPL’s historical return behavior, identify unusually large daily moves, and prepare the analysis for comparison with a market benchmark. It is also to describe how Apple’s stock performed over the selected period, using Python to organize the price data, calculate returns, and visualize the results.

### Questions

- How did AAPL’s adjusted price change over the sample period?
- How much did daily returns vary?
- What were the largest daily increase and decrease?
- How did large moves appear over time?

### Data

- **Source:** [Yahoo Finance historical data](https://finance.yahoo.com/quote/AAPL/history/)
- **Frequency:** Daily
- **Price series used for returns:** Adjusted Close
- **Tools:** Python, pandas, Matplotlib, Jupyter Notebook

### Methodology

1. **Data collection:** Download daily AAPL historical price data using Python.
2. **Data preparation:** Check the data, format the dates, sort records chronologically, and review missing or duplicate values.
3. **Price measure:** Use the adjusted closing price (`Adj Close`) to account for dividends and stock splits when measuring historical performance.
4. **Daily returns:** Calculate the percentage change in adjusted closing price from one trading day to the next:

   ```text
   Daily return (%) = (Current adjusted close / Previous adjusted close - 1) × 100

The notebook loads and checks the data, sorts observations by date, calculates daily adjusted-price returns, and plots the adjusted price and daily returns.

### Findings

- The dataset covers January 2, 2020, to November 17, 2026.
- The largest daily increase was **15.33% on April 9, 2025**.
- The largest daily decrease was **−12.86% on March 16, 2020**.
- The adjusted-price chart shows an overall upward trend with several declines and recoveries.
- Most daily returns are closer to zero than the largest positive and negative moves.

These findings describe the sample period. The notebook does not establish the causes of individual price movements or predict future returns.

### Limitations

- The analysis covers one company and does not yet compare AAPL with a market benchmark.
- Historical performance does not predict future performance.
- Large daily moves require additional research before attributing them to a specific event.
- The original data file is not included. Refer to the source and the notebook for the expected file name and format.

### Planned extension

The next version will compare AAPL with the S&P 500 and add drawdown and rolling-volatility analysis. These additions will help assess performance and risk relative to the broader market.

### Project files

- `aapl_analysis.ipynb` — data preparation, calculations, charts, and written interpretation
- `README.md` — project overview and findings

## 2. AAPL vs SPY: Historical Performance and Risk Analysis

### Project overview

This project compares Apple Inc. (AAPL) with SPY, an exchange-traded fund designed to track the S&P 500. It examines adjusted-price performance and historical risk from January 2, 2020 to November 17, 2026.

The analysis uses Python to prepare daily price data, calculate returns and risk measures, create charts, and summarize the results.

### Key findings

- AAPL’s cumulative adjusted-price return was **387.30%**, compared with **147.96%** for SPY.
- AAPL’s annualized return was **25.91%**, compared with **14.12%** for SPY.
- AAPL’s annualized volatility was **31.13%**, compared with **20.02%** for SPY.
- Maximum drawdowns were similar: **−33.36%** for AAPL and **−33.72%** for SPY.
- AAPL’s daily returns had a **0.749 correlation** with SPY and an estimated **beta of 1.165** over this sample.

In this historical period, AAPL had higher returns and more variable daily returns than SPY, while its maximum drawdown was similar. These findings describe the selected period and do not predict future performance.

### Charts

#### Growth of $100

![Growth of $100 in AAPL and SPY](images/aapl-vs-spy-growth.png)

#### Historical drawdowns

![Historical drawdowns for AAPL and SPY](images/aapl-vs-spy-drawdown.png)

#### Rolling volatility

![30-day rolling annualized volatility for AAPL and SPY](images/aapl-vs-spy-rolling-volatility.png)

### Method

- Used adjusted closing prices for AAPL and SPY.
- Matched the datasets on shared trading dates.
- Compared cumulative and annualized returns.
- Measured annualized volatility, maximum drawdown, 30-day rolling volatility, correlation, and beta.

### Data and how to run

- AAPL historical data: [Yahoo Finance](https://finance.yahoo.com/quote/AAPL/history/)
- SPY historical data: retrieved with the Python `yfinance` package.
- The raw AAPL Excel file is not included. Download the data and save it beside the notebook as `Historical Data Apple.xlsx`.
- Open `aapl_analysis.ipynb` in Jupyter and run the notebook cells from top to bottom. The SPY download requires an internet connection.

### Limitations

- This is a historical analysis, not a price forecast or buy-or-sell recommendation.
- SPY holds AAPL, so it is not fully independent of the stock being analyzed.
- The results cover one selected period and do not include an analysis of company financial statements, taxes, or an individual investor’s trading costs.
- Volatility, beta, and drawdown are historical estimates and can change across periods.

### Project files

- `aapl_analysis.ipynb` — data preparation, analysis, charts, and interpretation
- `images/` — exported charts used in this README
- `README.md` — project overview and findings
