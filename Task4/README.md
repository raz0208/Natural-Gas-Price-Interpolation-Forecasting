# Task 4: Strategic Bucketing of FICO Scores for PD Modeling
JPMorgan Chase & Co. Quantitative Research Virtual Experience Program on Forage


## Overview

This project focuses on the quantization of FICO credit scores to predict the **Probability of Default (PD)** for mortgage borrowers. The goal is to convert continuous FICO scores (ranging from 300 to 850) into optimized categorical buckets (ratings) for downstream machine learning models.

## Project Objective

Risk management models often require categorical data. This project solves the problem of mapping integer FICO scores into a fixed number of bins (ratings) while preserving the most predictive power regarding customer defaults.

## Methodology

The project implements a data-driven approach to determine optimal bucket boundaries using **Dynamic Programming**. Two specific optimization techniques are explored:

1. **Mean Squared Error (MSE) Minimization:** Approximates entries in a bucket to a single value by minimizing the squared error.
2. **Log-Likelihood Maximization:** A sophisticated probabilistic approach that maximizes the likelihood function based on the density of defaults within each bucket.

## Key Features

* **Data Analysis:** Exploration of FICO score distributions and rolling Probability of Default trends.
* **Algorithm Implementation:** Custom Python implementation of dynamic programming algorithms to split data into  optimal buckets.
* **Visualization:** Graphical representation of bucket boundaries and default rates.

## Dependencies

* Python 3.x
* Pandas
* NumPy
* Matplotlib / Seaborn (for visualization)
* Scikit-learn (optional, for metrics)

## Usage

The analysis is contained within the Jupyter Notebook `Strategic_Bucketing_of_FICO_Scores_for_PD_Modeling.ipynb`. Open the notebook to view the step-by-step logic from data ingestion to the generation of the final rating map.
