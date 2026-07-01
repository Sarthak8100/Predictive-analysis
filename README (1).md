# Predictive Analytics for Agronomic Data

## Overview
This repository contains an optimized machine learning pipeline designed to predict crop yields based on a comprehensive set of agronomic features. The system utilizes both standard predictive modeling and a robust nearest-neighbor fallback mechanism to handle anomalous client data.

This project was developed during a Research Internship under Prof. S. Chakraborty at IIT Kharagpur (Jan '26 - Mar '26).

## Data Features
The predictive models leverage a pre-processed dataset consisting of two primary feature categories:
* **Agrometeorological Features:** Includes environmental variables such as rainfall and temperature.
* **Edaphic (Soil) Features:** Includes soil chemistry and properties such as pH and N-P-K (Nitrogen, Phosphorus, Potassium) levels.

## Methodology & Tech Stack
* **Machine Learning Models:** Ridge Regression, Random Forest
* **Hyperparameter Tuning:** Bayesian Search via **Optuna**
* **Validation Strategy:** Rigorous 5-fold Cross-Validation (CV) to ensure model stability and generalizability.
* **Fallback Mechanism:** **FAISS** (Facebook AI Similarity Search) utilizing Manhattan distance was deployed as an efficient nearest-neighbor fallback for handling out-of-distribution or anomalous client data points.

## Performance
* **Cross-Validation $R^2$ Score:** 0.94 (demonstrating strong predictive stability).
