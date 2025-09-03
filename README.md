# Time-Series-Stock-Prediction
Stock price forecasting with ARIMA &amp; SARIMA complete time series workflow with stationarity tests, decomposition and model evaluation

# 📈 Stock Price Prediction using ARIMA & SARIMA

## 🔎 Overview
This project demonstrates how to forecast stock prices using **ARIMA** (AutoRegressive Integrated Moving Average) and **SARIMA** (Seasonal ARIMA) models.  
The notebook walks through **data preparation, stationarity testing, decomposition, model fitting, and forecasting** — with explanations for why each step matters.

---

## ⚙️ Why ARIMA and SARIMA?
- **ARIMA** is effective for time series that exhibit **trend** but no clear seasonal pattern.  
- **SARIMA** extends ARIMA by adding a **seasonal component**, making it suitable for series with **recurring cycles** (e.g., yearly, monthly, or weekly patterns).  
- Stock data often contains both **trend** (long-term growth/decline) and **seasonality** (recurring cycles), so comparing ARIMA vs. SARIMA helps evaluate which captures the dynamics better.

---

## 🛠️ Workflow

### 1. **Load the Data**
We start by importing stock price data (daily closing prices).  
- The **‘Close’ price** is usually the main target because it reflects the final value of the trading day.

---

### 2. **Test for Stationarity**
ARIMA/SARIMA models assume the series is **stationary**.  
- **Stationary series:** mean, variance, and autocorrelation stay constant over time.  
- Tests used:
  - **ADF (Augmented Dickey-Fuller):**  
    - Null Hypothesis (H₀): series is not stationary.  
    - Reject H₀ if *p-value < 0.05*.
    - ADF Test: checks if unit root exists.


  - **KPSS Test:**  
    - Null Hypothesis (H₀): series is stationary.  
    - Reject H₀ if *p-value < 0.05*.
    - KPSS Test: confirms if series is stationary.
- If not stationary, apply **differencing** or **log transformations**.









If p-value > 0.05 → series is not stationary → apply differencing/log transform.

### 3. **Time Series Decomposition**

- Break the series into:

- Trend → long-term growth/decline

- Seasonality → repeating cycles (e.g., yearly)

- Residuals → noise


- Additive Model: constant seasonal effect.

- Multiplicative Model: seasonal effect grows with trend.

### 4. **Build Models**
- ARIMA

- SARIMA

### 5. **Forecast & Evaluate**

- Generate forecasts

- Compare predicted vs actual

- Evaluate with RMSE/MAE

### **Key Learnings**

- Stationarity testing ensures ARIMA assumptions are met.

- Decomposition helps decide between additive vs multiplicative models.

- ARIMA works well for non-seasonal series.

- SARIMA captures recurring patterns (like yearly effects).

While stock markets are noisy, these models help uncover underlying structure.


Tech Stack

Python 

Pandas, NumPy (data processing)

Statsmodels (ARIMA, SARIMA, decomposition)

Matplotlib (visualization)
