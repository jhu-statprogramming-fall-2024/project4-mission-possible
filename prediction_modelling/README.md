# Clinical Trial Prediction Models

*Last updated: December 5, 2024*

## Overview

This repository contains LASSO models for predicting various aspects of clinical trials, such as country, disease, and phase predictions.

The goal is to provide accurate predictions using historical data, with a focus on predicting trends by years into the future.

## Programming paradigms

- Parallel computing paradigms
- Machine learning paradigms

## Model Performance
- Country Model: R-squared = 0.978, RMSE = 28.78
- Disease Model: R-squared = 0.752, RMSE = 23.69
- Phase Model: R-squared = 0.986, RMSE = 53.43

## Files
- `prediction_bundle.RData`: Contains all necessary components for predictions
  - LASSO models
  - Model evaluation results
  - Prediction function
  - Data splits

## Usage
```r
# Load prediction bundle
load("prediction_bundle.RData")

# Make predictions
prediction <- predict_trials(2025, "country", "United.States")