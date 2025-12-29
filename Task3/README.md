
---

# Task 3: Credit Risk Analysis: PD & EL Prediction
JPMorgan Chase & Co. Quantitative Research Virtual Experience Program on Forage


## Overview

This project focuses on building a predictive model for **Credit Risk** within a retail banking context. The goal is to estimate the **Probability of Default (PD)** for borrowers and calculate the **Expected Loss (EL)** on personal loans to assist the risk management team in setting appropriate loss allowances.

## Business Context

The retail banking arm has experienced higher-than-expected default rates. To mitigate future risks, this prototype uses historical borrower data to predict the likelihood of default.

The model outputs two key metrics:

1. **Probability of Default (PD):** The likelihood a borrower will stop making payments.
2. **Expected Loss (EL):** The financial loss anticipated, assuming a recovery rate of 10%.

## Methodology

The project follows a standard data science workflow:

* **Data Exploration (EDA):** Analyzing the distribution of income, debt, and loan characteristics.
* **Preprocessing:** Handling missing values and feature scaling.
* **Modeling:** Training a machine learning model (Gradient Boosting) to classify borrowers based on risk.
* **Risk Quantification:** Implementing a custom function to calculate expected financial loss.

## Usage

The core of the project is the `predict_expected_loss` function, which accepts specific borrower characteristics to generate a risk profile.

**Input Features:**

* Income
* Loan Amount
* Total Debt
* Number of Credit Lines
* Years Employed
* FICO Score

**Example Output:**

```json
{
    "Probability_of_Default": 0.15,
    "Expected_Loss": 704.83
}

```

## Technologies

* Python
* Pandas & NumPy (Data Manipulation)
* Scikit-Learn (Modeling)
* Matplotlib/Seaborn (Visualization)
