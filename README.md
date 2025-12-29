# Quantitative Finance & Risk Modeling Projects
JPMorgan Chase & Co. Quantitative Research Virtual Experience Program on Forage


## Overview

This repository contains a collection of **quantitative finance and risk analytics projects** developed to demonstrate applied skills in **time series modeling, derivative pricing, and credit risk modeling**.
The projects are motivated by real-world use cases from **commodity trading desks** and **banking risk management teams**, with an emphasis on **interpretable models, financial intuition, and practical implementation**.

The repository is organized into four core projects:

1. Natural Gas Price Forecasting & Interpolation
2. Natural Gas Storage Contract Pricing
3. Credit Risk Modeling (PD & Expected Loss)
4. Strategic Bucketing of FICO Scores for PD Modeling

Each project is self-contained and documented within its respective notebook(s).

---

## Project 1: Natural Gas Price Forecasting & Interpolation

### Objective

Analyze historical natural gas prices and build a framework to **estimate prices at any given date**, including:

* Interpolation between observed monthly prices
* Forecasting prices up to **one year into the future**

This project supports the valuation of **natural gas storage contracts**, where seasonal price behavior is critical.

### Key Components

* Exploratory Data Analysis (EDA)
* Seasonal decomposition (STL)
* Time-based interpolation
* ARIMA / SARIMA time series forecasting

### Key Insights

* Strong **annual seasonality**, with higher winter prices
* Clear trend and cyclical components
* Seasonal time series models produce realistic short-term forecasts

### Output

* A pricing function that returns an estimated gas price for any input date
* Supporting visualizations and one-year forward price projections

---

## Project 2: Natural Gas Storage Contract Pricing Prototype

### Objective

Develop a **prototype pricing tool** for valuing natural gas storage contracts by exploiting **seasonal price spreads**—buying gas in low-price periods and selling during high-demand months.

### Key Features

* Construction of a **continuous daily forward price curve**
* Storage contract valuation logic
* Detailed cost modeling, including:

  * Storage/rental fees
  * Injection and withdrawal costs
  * Transportation charges

### Implementation

* Jupyter Notebook–based interactive interface
* Users can input contract parameters such as:

  * Injection/withdrawal dates
  * Storage volume
  * Cost assumptions

### Output

* Estimated **net value of a storage contract**
* Scenario analysis for different seasonal strategies

---

## Project 3: Credit Risk Analysis – PD & Expected Loss Prediction

### Objective

Build a machine learning model to estimate:

1. **Probability of Default (PD)**
2. **Expected Loss (EL)** for retail banking personal loans

This project addresses rising default rates and supports **loss provisioning and risk-based decision making**.

### Methodology

* Exploratory Data Analysis (EDA)
* Data preprocessing and feature scaling
* Gradient Boosting classification model
* Custom Expected Loss calculation assuming a fixed recovery rate

### Model Inputs

* Income
* Loan amount
* Total debt
* Number of credit lines
* Years employed
* FICO score

### Output

```json
{
  "Probability_of_Default": 0.15,
  "Expected_Loss": 704.83
}
```

---

## Project 4: Strategic Bucketing of FICO Scores for PD Modeling

### Objective

Convert continuous FICO scores (300–850) into **optimal categorical risk buckets** for downstream PD models while preserving predictive power.

### Methodology

A **dynamic programming–based optimization approach** is used to determine bucket boundaries:

1. **Mean Squared Error (MSE) Minimization**
2. **Log-Likelihood Maximization** based on default densities

### Key Features

* Analysis of FICO score distributions and default trends
* Custom algorithm implementation (no black-box binning)
* Visualization of bucket boundaries and PD behavior

### Use Case

This approach mirrors industry practices where **ratings-based systems** are required for regulatory or model governance reasons.

---

## Technologies Used

* **Python**
* Pandas, NumPy
* Matplotlib / Seaborn
* Statsmodels (ARIMA / SARIMA)
* Scikit-learn
* Jupyter Notebook / Google Colab

---

## Intended Audience

* Quantitative Researchers
* Commodity Trading Analysts
* Risk Management & Credit Modeling Teams
* Students and professionals building applied finance portfolios

---

## Notes

Each notebook is designed to be:

* Reproducible
* Interpretable
* Closely aligned with real-world financial decision-making

This repository emphasizes **financial intuition combined with solid quantitative methods**, rather than purely academic modeling.

---

### For any inquiries or collaborations, feel free to reach out:

- Email: [raz02088@gmail.com](mailto:raz0208@gmail.com)
- LinkedIn: [Reza Azari Aghouieh](https://www.linkedin.com/in/reza-azari-aghoueh/)
