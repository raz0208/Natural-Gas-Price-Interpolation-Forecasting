## **Task1: Natural Gas Price Forecasting – Code Review & Analysis Report**
--- JPMorgan Chase & Co. Quantitative Research Virtual Experience Program on Forage ---

### Project Objective

The objective of this project is to analyze historical monthly natural gas prices and build a robust framework to estimate gas prices at any arbitrary date in the past and extrapolate prices one year into the future.
This supports the pricing of natural gas storage contracts, where accurate estimation of purchase and withdrawal prices—especially across seasons—is critical for profitability and risk management.

---

### Dataset

* **Source**: Monthly natural gas price snapshots from a market data provider
* **Frequency**: Monthly (end-of-month prices)
* **Time Span**:

  * From **31 October 2020**
  * To **30 September 2024**
* **Structure**:

  * `Dates`: Month-end delivery dates
  * `Prices`: Natural gas prices at those dates

The dataset combines **historical realized prices** with **forward-looking monthly snapshots**, forming a continuous time series suitable for trend and seasonality analysis.

---

### Models Implemented

The notebook implements a **hybrid statistical time-series approach**, focused on interpretability and financial relevance rather than black-box prediction:

1. **Time-Series Interpolation**

   * Used to estimate gas prices for **any date between known monthly observations**
   * Ensures smooth price curves instead of stepwise monthly prices

2. **Seasonal Decomposition (STL)**

   * Decomposes the price series into:

     * **Trend**
     * **Seasonal**
     * **Residual** components
   * Enables clear identification of recurring seasonal effects

3. **Forecasting via Trend + Seasonality Extension**

   * The trend component is extrapolated forward
   * Seasonal patterns are repeated for future months
   * Produces **indicative monthly prices for one additional year**

This modeling choice aligns well with **commodity markets**, where seasonality is persistent and economically driven.

---

### Visual Analysis

The notebook includes multiple visualizations that reveal key market behaviors:

* **Time-Series Line Plot**

  * Shows a clear **upward trend** in prices from 2020 to 2024
  * Highlights increased volatility during certain periods

* **Seasonality Patterns**

  * Prices tend to **increase during winter months**
  * Reflects higher heating demand and storage drawdowns
  * Lower prices are generally observed during summer injection periods

* **STL Decomposition Plots**

  * Trend: Long-term structural increase in prices
  * Seasonal: Stable, repeating annual cycle
  * Residuals: Short-term shocks and noise

These visual insights justify the use of **seasonally-aware pricing models** for storage contracts.

---

* **Forecasting Assumption**

  * Seasonal effects repeat annually
  * Trend evolves smoothly over time

This mathematical structure ensures **financial interpretability**, which is essential for trading and risk discussions.

---

### Final Deliverables

* A **Python-based pricing function** that:

  * Takes a date as input
  * Returns an estimated natural gas price
* Historical price interpolation for **any past date**
* Forward price extrapolation for **one additional year**
* Clear visual diagnostics supporting model assumptions
* A reproducible notebook suitable for:

  * Trading desk analytics
  * Storage contract valuation
  * Scenario analysis and stress testing

---

This project demonstrates a **practical, desk-ready approach** to commodity price modeling, balancing statistical rigor with transparency—well aligned with quantitative research expectations in energy trading environments.
