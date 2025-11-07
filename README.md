Time Series Analysis of Hourly Energy Demand
🧠 Project Overview

This project focuses on analyzing and forecasting hourly energy demand using statistical and machine learning–based time series models.
The goal is to identify underlying patterns, test for stationarity, evaluate model assumptions, and develop accurate forecasting models to predict future energy consumption trends.

The study follows a systematic approach of data preprocessing, stationarity testing, model development, residual analysis, and evaluation using multiple performance metrics.

📂 Dataset Information

Source: NITI Aayog – Government of India

Description: The dataset contains hourly electricity demand readings from national energy records.

Purpose: To understand temporal variations in energy consumption and forecast future demand.

Frequency: Hourly

Data Format: Time-indexed CSV/Excel data

🧪 Statistical Tests Performed
1. Augmented Dickey-Fuller (ADF) Test

Used to check stationarity in time series data.

H₀: Data is non-stationary

H₁: Data is stationary
Performed before and after differencing to ensure stationarity.

2. Kwiatkowski–Phillips–Schmidt–Shin (KPSS) Test

Complements ADF by testing the opposite hypothesis.

H₀: Data is stationary

H₁: Data is non-stationary

3. Ljung–Box Test

Used to check autocorrelation in residuals after model fitting.
If p-value > 0.05 → residuals are independent (no autocorrelation).

🔍 Analytical Steps
Residual Analysis

Conducted after model fitting to ensure white noise behavior:

Checked residual mean and variance stability

Plotted residual distribution

Performed Ljung–Box test to confirm randomness

Time Series Decomposition

Decomposed data into trend, seasonal, and residual components to visualize long-term patterns.

📈 Visualization & Plots
Plot Type	Description
ACF Plot (Autocorrelation Function)	Identifies lag correlations (for AR terms).
PACF Plot (Partial Autocorrelation Function)	Helps determine MA terms.
Actual Forecast Plot	Compares actual vs predicted energy demand.
Residual Forecast Plot	Shows randomness and residual behavior.
Predicted Forecast Plot	Displays the future forecast curve.

These visualizations guided model selection and evaluation.

🤖 Models Implemented
1. ARIMA (AutoRegressive Integrated Moving Average)

Baseline forecasting model for univariate time series.

Parameters (p, d, q) tuned via ACF/PACF analysis.

Evaluated using AIC/BIC and forecast error metrics.

2. SARIMA (Seasonal ARIMA)

Handles both trend and seasonality.

Seasonal parameters (P, D, Q, m) optimized using AIC/BIC.

Demonstrated better accuracy for cyclical energy demand.

3. Prophet (Meta/Facebook)

Captures complex patterns automatically (trend + seasonality).

Produces interpretable and visually rich forecasts.

📊 Model Evaluation Metrics
Metric	Description
AIC	Model fit quality (lower = better).
BIC	Penalizes overly complex models (lower = better).
RMSE	Measures average magnitude of error.
MSE	Average squared prediction error.
MAPE	Accuracy as a percentage (lower = better).

SARIMA and Prophet performed best based on these metrics.

⚙️ Workflow Summary

Data Import from NITI Aayog

Data Cleaning and Indexing

Visualization of Hourly Demand

Stationarity Tests (ADF, KPSS)

ACF/PACF Analysis

Model Building (ARIMA, SARIMA, Prophet)

Model Diagnostics & Residual Analysis

Forecasting & Evaluation (AIC, BIC, RMSE, MAPE)

🚀 Key Insights

Strong daily and weekly seasonality detected.

SARIMA outperformed ARIMA for short-term forecasts.

Prophet captured long-term seasonality well.

Residuals confirmed model validity and randomness.
