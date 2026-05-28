# Global Temperature Forecasting
### Machine Learning & Time-Series Techniques

A complete end-to-end data science project that analyses **175 years of global surface temperature data** (1850–2026) and builds multiple forecasting models to predict future climate trends.

## Project Highlights

- **Zero data preprocessing headaches** — uses the NOAA GCAG dataset with no missing values
- **5 models compared** — Linear Regression, Random Forest, SVR, ARIMA, and Facebook Prophet
- **Hyperparameter tuning** via GridSearchCV (not arbitrary defaults)
- **Proper time-series methodology** — no-shuffle train/test split, lag features, stationarity testing
- **Future forecast** up to 2030 with a correctly implemented rolling prediction loop

## Dataset

| Property | Details |
|---|---|
| Source | [NOAA GCAG via datahub.io](https://datahub.io/core/global-temp) |
| Coverage | January 1850 — present (updated monthly) |
| Rows | ~2,100+ months |
| Missing values | **None** |
| Target variable | Temperature anomaly (°C deviation from 20th-century average) |

> **No download required.** The dataset is fetched automatically inside the notebook via a single URL.

## Models Used

| Model | Type | Notes |
|---|---|---|
| Linear Regression | ML Baseline | Interpretable, fast |
| Random Forest | ML Ensemble | Best accuracy; tuned with GridSearchCV |
| SVR | ML Kernel | Robust to outliers |
| ARIMA(2,1,2) | Classical Time-Series | Principled sequential model |
| Facebook Prophet | Time-Series | Handles trend + seasonality automatically |

## Project Structure

```
global-temperature-forecasting/
│
├── Weather_Forecasting_NOAA_Portfolio.ipynb   
├── requirements.txt                           
├── README.md                                  
└── .gitignore                                 
```

## 📈 Key Findings

- Global surface temperatures have risen **+1.3°C** above the 20th-century baseline
- Warming rate since 1980 is approximately **+0.2°C per decade**
- Random Forest achieved the best predictive accuracy on test data
- The 12-month lag feature was the most important predictor, capturing annual seasonality

## 🛠️ Tech Stack

- **Python 3.10+**
- `pandas`, `numpy` — data manipulation
- `matplotlib`, `seaborn` — visualisation
- `scikit-learn` — ML models and evaluation
- `statsmodels` — ARIMA, ADF test, seasonal decomposition
- `prophet` — Facebook Prophet forecasting
