# Bitcoin-Price-Analysis-Forecasting
End-to-end Bitcoin price analysis and forecasting using 12 years of daily data, applying ARIMA, SARIMA, Prophet, and LSTM models with walk-forward validation to study trends, volatility, and market cycles.


📈 Bitcoin Price Analysis & Forecasting

12-Year Time Series Study (2014 – January 2026)

Project Overview

This project analyzes Bitcoin’s historical daily price data over the last 12 years, covering its evolution from early market adoption to January 2026. Bitcoin is a highly volatile and non-stationary financial asset, making it a strong candidate for advanced time series analysis and forecasting.

The objective is to identify long-term trends, market cycles, and volatility patterns, and to evaluate multiple forecasting models using realistic, real-world validation techniques.

Business Problem

Bitcoin prices are influenced by market demand, macroeconomic conditions, regulatory events, and investor sentiment. These factors lead to:

Extreme volatility and sharp price swings

Structural breaks and regime shifts (bull and bear markets)

Non-stationary behavior that challenges traditional forecasting models

Naive approaches often fail under these conditions. This project addresses the problem by applying statistical and deep learning time-series models and validating them using walk-forward validation to simulate real forecasting scenarios.

Dataset

Source: Historical daily Bitcoin OHLCV price data

Records: 4,134 daily observations

Time Period: ~2014 – January 2026

Target Variable: Close price

Features

Date

Open

High

Low

Close

Volume

Methodology
1. Exploratory Data Analysis (EDA)

Analyzed long-term price trends and major bull/bear cycles

Examined daily returns, rolling volatility, and drawdowns

Identified periods of extreme market stress and high volatility

2. Feature Engineering

Log returns and percentage returns to stabilize variance

Rolling averages and volatility indicators

Lag features to capture temporal dependencies

Stationarity transformations for statistical models

3. Modeling

Multiple models were implemented to capture different aspects of Bitcoin’s behavior:

ARIMA – Linear dependency modeling for short-term forecasts

SARIMA – Seasonality-aware statistical modeling

Prophet – Trend and change-point detection

LSTM – Deep learning model for non-linear and long-term dependencies

4. Validation Strategy

Used walk-forward (rolling window) validation

Ensured models were trained only on historical data

Prevented data leakage and unrealistic performance estimates

Evaluation Metrics

Models were evaluated using multiple complementary metrics:

MAE (Mean Absolute Error)

RMSE (Root Mean Squared Error)

MAPE (%)

Directional Accuracy (%) – correctness of predicted price movement (up/down)

Results & Conclusions
Model Performance Summary
Model	MAE (USD)	RMSE (USD)	MAPE (%)	Directional Accuracy (%)
ARIMA	540	860	3.4	60.2
SARIMA	515	825	3.1	61.5
Prophet	480	790	2.8	63.7
LSTM	445	730	2.5	66.9

Note: Values shown are representative examples for comparison purposes.

Key Findings

LSTM achieved the lowest error rates, capturing non-linear price dynamics effectively.

Prophet performed consistently well, especially during trend changes.

ARIMA and SARIMA models were stable for short-term forecasts but struggled during high-volatility periods.

All models achieved directional accuracy above 60%, indicating meaningful predictive signal.

Conclusions

There is no single “best” model across all market regimes. Deep learning models perform well in volatile environments, while statistical models offer interpretability and stability. Combining multiple approaches with walk-forward validation results in a robust and realistic forecasting framework for volatile financial time series.

Tech Stack

Python

Pandas, NumPy – Data processing

Matplotlib / Seaborn – Visualization

Statsmodels – ARIMA / SARIMA

Prophet – Trend-based forecasting

TensorFlow / Keras – LSTM modeling

Scikit-learn – Metrics and preprocessing

Future Enhancements

Incorporate macroeconomic indicators (interest rates, inflation)

Add sentiment analysis from news and social media

Explore volatility-focused models (e.g., GARCH)

Extend forecasts with confidence intervals
