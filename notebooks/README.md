# Notebooks

Notebooks
This folder contains Jupyter notebooks illustrating the step-by-step process of analyzing historical performance, volatility, and risk metrics for TSLA, BND, and SPY, preparing the data for further portfolio modeling.

### 1_TSLA_BND_SPY_Analysis.ipynb

- Downloaded daily OHLCV and adjusted close data (2015–2025) from yfinance
- Cleaned and aligned datasets, handled missing values, and verified data types
- Calculated daily returns and conducted exploratory data analysis (EDA)
- Visualized price trends, return distributions, and rolling volatility patterns
- Identified outlier days with extreme returns
- Tested stationarity of prices and returns using the Augmented Dickey-Fuller (ADF) test
- Computed key risk metrics: annualized return, volatility, Sharpe ratio, and Value at Risk (VaR)
- Summarized findings to inform portfolio risk/return trade-off analysis