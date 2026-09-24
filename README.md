# Exchange Rate Forecasting

## Project Overview

This project investigates exchange rate forecasting using a comparative set of time series and machine learning approaches. The analysis focuses on five currency pairs: EUR/USD, USD/JPY, USD/INR, GBP/USD, and AUD/USD.

Daily exchange rate data were aggregated to monthly averages and combined with macroeconomic variables including the U.S. Dollar Index (DXY), Brent crude oil prices, Consumer Price Index (CPI), Federal Funds Rate, and Trade Balance.

The project compares traditional time series models with machine learning approaches and examines volatility dynamics in exchange rate movements.

## Objectives

- Analyse historical exchange rate movements across multiple currency pairs.
- Examine stationarity, autocorrelation, volatility, and relationships with macroeconomic variables.
- Compare ARIMA, ARIMAX, and VAR time series models.
- Compare Random Forest, XGBoost, and LSTM models for forecasting.
- Evaluate XGBoost performance across multiple currency pairs.
- Model exchange rate volatility using GARCH.
- Use Diebold-Mariano tests to compare forecasting performance between selected models.

## Data

The project uses monthly data derived from daily exchange rates and macroeconomic indicators.

### Exchange Rates

- EUR/USD
- USD/JPY
- USD/INR
- GBP/USD
- AUD/USD

### Macroeconomic Variables

- DXY
- Brent Crude Oil
- Federal Funds Rate
- Consumer Price Index
- Trade Balance

The original datasets are provided in the `data/` directory.

## Methodology

The analysis follows these main stages:

1. Data cleaning and preprocessing
2. Monthly aggregation and dataset merging
3. Exploratory data analysis
4. Stationarity testing using the Augmented Dickey-Fuller test
5. Differencing and log-return analysis
6. ACF and PACF analysis
7. Time series modelling
8. Machine learning based forecasting
9. Volatility modelling
10. Statistical comparison of forecasting errors

## Models

### Time Series Models

- ARIMA
- ARIMAX
- VAR

### Machine Learning Models

- Random Forest
- XGBoost
- LSTM

### Volatility Model

- GARCH(1,1)

## Notebook Structure

### `01_data_preparation_and_eda.ipynb`

Covers:

- Data loading and cleaning
- Monthly aggregation
- Dataset merging
- Exploratory analysis
- Correlation analysis
- Stationarity testing
- Differencing
- ACF/PACF analysis
- Log-return analysis

### `02_time_series_models.ipynb`

Covers:

- ARIMA modelling
- ARIMAX modelling
- VAR modelling
- Forecast evaluation

### `03_machine_learning_and_lstm.ipynb`

Covers:

- Random Forest
- XGBoost
- LSTM
- XGBoost forecasting across additional currency pairs

### `04_volatility_and_model_comparison.ipynb`

Covers:

- GARCH model selection
- GARCH(1,1) volatility modelling
- Diebold-Mariano forecast comparison tests

## Results

For the EUR/USD forecasting task, the implemented models produced the following test-set RMSE values:

| Model | RMSE |
|---|---:|
| ARIMA | 0.114944 |
| ARIMAX | 0.072477 |
| Random Forest | 0.0612 |
| XGBoost | 0.032181 |

The project also evaluates forecasting performance for USD/JPY, USD/INR, GBP/USD, and AUD/USD using XGBoost.

The notebooks contain the detailed evaluation metrics, statistical tests, visualisations, and model outputs.

## Project Structure

```text
exchange-rate-forecasting/
│
├── README.md
├── .gitignore
│
├── notebooks/
│   ├── 01_data_preparation_and_eda.ipynb
│   ├── 02_time_series_models.ipynb
│   ├── 03_machine_learning_and_lstm.ipynb
│   └── 04_volatility_and_model_comparison.ipynb
│
└── data/
    ├── EURUSD.csv
    ├── USDJPY.csv
    ├── USDINR.csv
    ├── GBPUSD.csv
    ├── AUDUSD.csv
    ├── DXY.csv
    ├── DCOILBRENTEU.csv
    ├── FEDFUNDS.csv
    ├── CPIAUCSL.csv
    └── BOPGSTB.csv
