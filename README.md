# Volatility-Driven Asset Allocation: GARCH & ARIMA Backtesting

Walk-forward backtesting framework comparing GARCH(1,1) conditional volatility against historical volatility for risk-tier classification (conservative/moderate/aggressive) on the S&P 500 universe. Extended with variance-covariance clustering for structural stock selection, aggregated into a meta-strategy benchmarked against a Minimum Variance portfolio.

**Course:** Laboratory of Data Analytics for Investment, Università Cattolica

**Datasets:** Provided by the course (Laboratory of Data Analytics for Investment). Not redistributed here due to licensing restrictions. Includes historical S&P 500 constituent return metrics and a time-varying composition matrix (binary flag, 1 if a stock was a member of the index at time t, 0 otherwise — used to eliminate survivorship bias in the backtest).

**Methodology:**
- Walk-forward backtest, weekly rebalancing, no look-ahead or survivorship bias
- GARCH(1,1) vs. historical volatility for tertile-based risk classification
- ARIMA(1,0,0) as fallback when GARCH fails to converge
- Variance-covariance matrix clustering for stock selection within risk tiers
- Meta-strategy (aggregated risk classes) vs. Minimum Variance S&P 500 benchmark

**Results:**
- Meta-strategy weekly Sharpe ratio: 0.083 vs. 0.038 (benchmark) — computed on unannualized weekly returns
- Cumulative return: +135.6% vs. +71.4% (benchmark)
- Methodology later extended in my master's thesis with HMM-based regime detection and fuzzy logic risk classification

**Files:**
**Files:**
- `investment.ipynb` — full analysis code (Python)
- `Volatility-Driven_Asset_Allocation...pdf` — presentation slides (large file, download to view — inline preview may fail)

