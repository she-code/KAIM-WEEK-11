# Time Series Forecasting for Portfolio Management Optimization 

## Project Overview

This project develops a time series forecasting system for Guide Me in Finance (GMF) Investments to optimize portfolio management. Using historical and real-time market data from yfinance, the model forecasts returns, volatility, and momentum signals to support informed asset allocation. The forecasts serve as one input within GMF’s broader investment strategy, helping analysts adjust portfolios, manage risk, and capitalize on market opportunities.

---

## Project Structure

```
KAIM-WEEK-11/
├── .github/
│ └── workflows/ # GitHub Actions workflows
├── data/
│ ├── raw/ # Raw data (should never be modified)
│ └── processed/ # Processed/cleaned data (gitignored)
├── models/
├── notebooks/
│ └── README.md # Documentation for notebooks
│ └── 1_TSLA_BND_SPY_Analysis.ipynb - fetches finance data from yfinance 
│ └── 2_TSLA_Forecasting_Models.ipynb - builds and compares models 
│ └── 3_TSLA_Future_Forecast_Analysis.ipynb - 6 months tsla forecast using lsmt
├── scripts/
│ └── README.md # Documentation for scripts
├── src/
│ └── utils/ # Utility functions
│  │ └── data_loader.py # loads csv files
├── tests/
│ └── __init__.py # 
│ └── README.md # Testing documentation
├── vector_store/
│ └── chroma.sqlite3
├── .gitattributes
├── .gitignore
├── README.md # Main project documentation
└── requirements.txt # Python dependencies
```
---
## 🛠 Tools & Technologies

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn (visualization)  
- Jupyter Notebook  
- Git  
- YFinance
- Tensorflow

---

## Key Task Completed 

### ✅ Task 1: Preprocess and Explore the Data

Downloaded TSLA, BND, and SPY daily OHLCV data (2015–2025) via yfinance. Cleaned and aligned datasets, handled missing values, and calculated daily returns. Visualized prices, returns, and rolling volatility. Identified outliers, tested stationarity (ADF), and computed key risk metrics (annualized returns, volatility, Sharpe ratio, VaR).

### ✅ Task 2: Develop Time Series Forecasting Models

Implemented and compared ARIMA and LSTM models to forecast TSLA stock prices (2015–2025). The dataset was split chronologically into training (2015–2023) and testing (2024–2025) sets. After preprocessing and normalization, an ARIMA(2,1,2) model was developed using ACF/PACF for parameter selection. A deeper LSTM model with two 50-unit layers and a 30-day lookback window was trained with early stopping to avoid overfitting. Model evaluation showed LSTM’s superior accuracy, achieving an MAE of $13.66 (82% lower than ARIMA) and a MAPE of 4.89%. The notebook includes visualizations of predicted versus actual prices, a detailed model comparison, and saving the best LSTM model (best_lstm_model.keras) along with its scaler for deployment. Key insights emphasize LSTM’s strength in capturing TSLA’s non-linear price dynamics versus ARIMA’s interpretability but lower accuracy.

### ✅ Task 3: Forecast Future Market Trends

Generated 6-month TSLA price forecasts using the trained LSTM model, starting from the most recent 30 days of market data. Created business-day predictions with confidence bands, identifying key support/resistance levels and potential trading opportunities. Analyzed forecasted trends and volatility patterns, saving results to CSV for future reference. Documented model limitations including decaying accuracy beyond 3 months and lack of fundamental data integration.

---

## ⚙️ Setup Instructions

1. **Clone the repository:**

```bash
git clone https://github.com/she-code/KAIM-WEEK-11
cd KAIM-WEEK-11
```

2. **Create and activate a virtual environment:**

```bash
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate
```
3. **Install dependencies:**

```bash
pip install -r requirements.txt

```
---
## Contributors
- Frehiwot Abebie
