# Vehicle Performance Modelling. Machine Learning Benchmark

A Python-based machine learning project exploring regression techniques for predicting vehicle lap times from simulated operating parameters.

## Overview

This project compares different regression approaches for modelling vehicle performance under varying tyre age, track temperature, fuel load and downforce conditions.

The goal is to evaluate predictive accuracy, investigate nonlinear relationships and understand how model selection affects performance.

All data is synthetically generated for educational purposes. The project does not use real Formula 1 metrics.

## Methods

* Python, NumPy, Pandas and scikit-learn
* Linear Regression
* Random Forest Regression
* Polynomial Regression with Ridge regularisation
* Train/test evaluation and 5-fold cross-validation
* Residual analysis
* Permutation feature importance


## Results

| Model | Test MAE (s) | Test R² | Cross-validation MAE (s) |
|---|---:|---:|---:|
| Linear Regression | 0.4198 | 0.9230 | 0.4146 |
| Random Forest | 0.2542 | 0.9696 | 0.2663 |
| **Polynomial Regression** | **0.1970** | **0.9827** | **0.2046** |

Polynomial Regression achieved the lowest prediction error, demonstrating the importance of selecting a model that matches the underlying structure of the data.

## Key Findings

* Nonlinear tyre degradation significantly affected simulated lap-time predictions.
* Polynomial Regression outperformed the other evaluated models.
* Cross-validation showed consistent performance across five training-data folds.
* Permutation importance identified tyre age and fuel load as the most influential predictive features in the synthetic dataset.

## Limitations

The dataset is generated using simplified mathematical relationships and does not show real vehicle dynamics or measured racing telemetry. Results should be interpreted as a machine-learning method demonstration rather than a validated performance model.

## Future Improvements

* Evaluate models using real, publicly available motorsport data.
* Introduce additional vehicle and environmental parameters.
* Explore more advanced feature engineering and hyperparameter optimisation.
* Investigate model generalisation under changing track conditions.
