# Apple Inc. (AAPL): Return and Performance Analysis

## Project overview

This project examines Apple Inc. (AAPL) daily historical prices from January 2, 2020, to November 17, 2026. Using Python, pandas, and Matplotlib, it explores the performance, adjusted-price movements and daily returns. The goal is to describe AAPL’s historical return behavior, identify unusually large daily moves, and prepare the analysis for comparison with a market benchmark.

## Questions

- How did AAPL’s adjusted price change over the sample period?
- How much did daily returns vary?
- What were the largest daily increase and decrease?
- How did large moves appear over time?

## Data and methods

- **Source:** [Yahoo Finance historical data](https://finance.yahoo.com/quote/AAPL/history/)
- **Frequency:** Daily
- **Price series used for returns:** Adjusted Close
- **Tools:** Python, pandas, Matplotlib, Jupyter Notebook

The notebook loads and checks the data, sorts observations by date, calculates daily adjusted-price returns, and plots the adjusted price and daily returns.

## Findings

- The dataset covers January 2, 2020, to November 17, 2026.
- The largest daily increase was **15.33% on April 9, 2025**.
- The largest daily decrease was **−12.86% on March 16, 2020**.
- The adjusted-price chart shows an overall upward trend with several declines and recoveries.
- Most daily returns are closer to zero than the largest positive and negative moves.

These findings describe the sample period. The notebook does not establish the causes of individual price movements or predict future returns.

## Limitations

- The analysis covers one company and does not yet compare AAPL with a market benchmark.
- Historical performance does not predict future performance.
- Large daily moves require additional research before attributing them to a specific event.
- The original data file is not included. Refer to the source and the notebook for the expected file name and format.

## Planned extension

The next version will compare AAPL with the S&P 500 and add drawdown and rolling-volatility analysis. These additions will help assess performance and risk relative to the broader market.

## Project files

- `aapl_analysis.ipynb` — data preparation, calculations, charts, and written interpretation
- `README.md` — project overview and findings
