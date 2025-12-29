## **Task1: Natural Gas Price Forecasting – Code Review & Analysis Report**
JPMorgan Chase & Co. Quantitative Research Virtual Experience Program on Forage

### Project Overview

This project analyzes historical monthly natural gas prices and builds a framework to **estimate prices at any given date**, including **interpolation between known prices** and **forecasting one year into the future**. The work is motivated by the need to price **natural gas storage contracts**, where seasonal price behavior plays a key role.

The analysis combines exploratory visualization with classical time series modeling to capture **trend, seasonality, and temporal dependencies** in natural gas prices.

---

## Dataset

* Monthly natural gas prices (end-of-month delivery)
* Time range: **October 2020 – September 2024**
* Data includes historical prices and forward market snapshots
* Each observation represents the market price at the end of a calendar month

---

## Methodology

* **Exploratory Data Analysis (EDA)** to identify trends and seasonal effects
* **Time-based interpolation** to estimate prices for non-month-end dates
* **Seasonal decomposition (STL)** to separate trend, seasonality, and noise
* **ARIMA / SARIMA models** to forecast prices up to **one year ahead**

The models are designed to respect the strong **annual seasonality** typical of natural gas markets.

---

## Key Insights

* Natural gas prices exhibit **clear seasonal patterns**, with higher prices in winter months
* Trend components capture medium-term market shifts
* Seasonal time series models provide realistic short- to medium-term forecasts

---

## Output

* A pricing function that takes a **date as input** and returns an estimated gas price
* Visualizations supporting trend and seasonality assumptions
* One-year forward price extrapolation beyond the available data

---

## Tools & Technologies

* Python
* Pandas, NumPy
* Matplotlib
* Statsmodels (ARIMA / SARIMA)

---

## Use Case

This project is intended for **quantitative research and commodity trading applications**, particularly for valuing **natural gas storage contracts** that depend on seasonal price differentials.

