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

For AAPL Historical Price and Performance Analysis, we use a descriptive, time-series analysis: we examine past prices and returns to summarize what happened during the selected period.

This section uses descriptive time-series analysis to examine Apple's historical stock prices and daily returns.

1. **Data collection:** Download daily AAPL historical price data using Python.
2. **Data preparation:** Check the data, format the dates, sort records chronologically, and review missing or duplicate values.
3. **Price measure:** Use the adjusted closing price (`Adj Close`) to account for dividends and stock splits when measuring historical performance.
4. **Daily returns:** Calculate the percentage change in adjusted closing price from one trading day to the next:

   ```text
   Daily return (%) = (Current adjusted close / Previous adjusted close - 1) × 100

5. **Analysis and visualization** Plot adjusted closing prices and daily returns, summarize return patterns, and identify the largest daily gain and loss in the dataset.

### Findings

#### 1. The dataset covers January 2, 2020 to November 17, 2026.

#### 2. The largest daily increase was **15.33% on April 9, 2025**.

AAPL rose **15.33%** on April 9, 2025, during a sharp market-wide rebound. The U.S. announced a 90-day pause on certain tariffs for many trading partners, easing some investor concerns about trade and supply-chain costs. China was excluded from the pause, so trade uncertainty affecting Apple did not disappear.

**Interpretation:** The tariff announcement likely contributed to the rally by improving investor expectations that trade tensions with many countries might ease. This is a market-context explanation, not proof that one announcement alone caused Apple's entire price move.

#### 3. The largest daily decrease was **−12.86% on March 16, 2020**.

AAPL fell **12.86%** on March 16, 2020, during a severe market sell-off as the COVID-19 outbreak raised fears of widespread business disruption and recession. The Federal Reserve had announced emergency measures the day before, including cutting its benchmark interest rate to near zero. However, investors remained concerned about the pandemic's economic effects, and U.S. stocks fell sharply.

**Interpretation:** The decline appears to have happened amid broad market panic, rather than being evidence by itself of an Apple-specific problem. The timing provides context, but it does not prove exactly what caused AAPL's entire daily move.

#### 4. The adjusted-price chart shows an overall upward trend with several declines and recoveries.

#### 5. Most daily returns are closer to zero than the largest positive and negative moves.

These findings describe the sample period. The notebook does not establish the causes of individual price movements or predict future returns.

### Limitations

- The analysis covers one company and does not yet compare AAPL with a market benchmark.
- Historical performance does not predict future performance.
- Large daily moves require additional research before attributing them to a specific event.
- The original data file is not included. Refer to the source and the notebook for the expected file name and format.


## 2. AAPL vs SPY: Historical Performance and Risk Analysis

### Project overview

This section compares Apple's historical performance with SPY, an ETF designed to track the S&P 500, over the same date range. The comparison shows how AAPL performed relative to a broad U.S. large-company market benchmark.

To make the price trends easier to compare, both investments are rebased to a starting value of $100. The analysis also examines daily returns, annualized return, annualized volatility, maximum drawdown, rolling volatility, correlation, and beta.

The results help describe the trade-off between historical return and risk in this sample. They are historical measurements, not predictions or investment recommendations.

### Data

- AAPL and SPY historical data: [Yahoo Finance](https://finance.yahoo.com/quote/AAPL/history/) and retrieved with the Python `yfinance` package.
- Open `aapl_analysis.ipynb` in Jupyter and run the notebook cells from top to bottom.

### Methodology

For this comparison, we use benchmark-relative performance and risk analysis. The key is to compare both assets over the same dates and calculate their returns from adjusted prices.

1. **Collect and prepare the data:** Download daily AAPL and SPY price data, convert dates to a consistent format, and sort both datasets chronologically.
2. **Align the comparison period:** Match AAPL and SPY on their shared trading dates so the comparison uses the same observations.
3. **Use adjusted closing prices:** Calculate returns from adjusted closing prices to account for dividends and stock splits.
4. **Compare investment growth:** Rebase both price series to $100 at the start of the shared period. This shows how the value of a hypothetical $100 investment would have changed over time.
5. **Calculate daily returns:** Use the percentage change in adjusted closing prices from one trading day to the next.
6. **Measure performance and risk:**
   - **Cumulative return:** Total percentage gain or loss over the comparison period.
   - **Annualized return (CAGR):** Compounded average annual growth over the period.
   - **Annualized volatility:** Standard deviation of daily returns multiplied by the square root of 252 trading days.
   - **Maximum drawdown:** Largest percentage decline from a previous peak in the adjusted-price series.
   - **Rolling 30-day volatility:** Annualized volatility calculated over successive 30-trading-day windows.
   - **Correlation:** Measures how closely AAPL and SPY daily returns moved together.
   - **Beta:** Estimates AAPL's historical sensitivity to SPY's daily returns, calculated as the covariance of their returns divided by SPY's return variance.
7. **Visualize and interpret:** Use growth, drawdown, and rolling-volatility charts alongside a summary table to compare historical performance and risk.

This is a descriptive analysis of historical data, not a forecast or investment recommendation. SPY includes Apple among its holdings, so the two investments are related rather than fully independent.

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
