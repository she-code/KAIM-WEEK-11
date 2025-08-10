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
├── notebooks/
│ └── README.md # Documentation for notebooks
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

---

## Key Task Completed 

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
