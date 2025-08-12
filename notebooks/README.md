# Notebooks
- 
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

### 2_TSLA_Forecasting_Models.ipynb

- Implemented and compared ARIMA (2,1,2) and LSTM models for TSLA price forecasting
- Performed train-test split (2015-2023 train, 2024-2025 test) preserving temporal order
- Optimized ARIMA parameters via ACF/PACF analysis and manual tuning
- Designed LSTM architecture with 2 layers (50 units each) and 30-day lookback window
- Evaluated models using MAE, RMSE, and MAPE metrics
- Visualized predictions vs actuals with confidence intervals (ARIMA) and prediction bands
- Selected LSTM as best model (MAE: $13.66, MAPE: 4.89%) and saved for deployment

### 3_TSLA_Future_Forecast_Analysis.ipynb

- Generated 6-month LSTM forecast using best model
- Prepared input from last 30 days of TSLA data
- Created business-day timeline (126 trading days)
- Visualized forecast with confidence bands (±1 std dev)
- Identified key levels: support/resistance zones
- Saved results as TSLA_6mo_forecast.csv
- Noted model limitations for risk awareness