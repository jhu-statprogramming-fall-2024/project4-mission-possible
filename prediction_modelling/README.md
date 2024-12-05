# Clinical Trial Prediction Models

*Last updated: December 5, 2024*

## Overview

This repository contains LASSO models for predicting various aspects of clinical trials, such as country, disease, and phase predictions.

The goal is to provide accurate predictions using historical data, with a focus on predicting trends up to 3 years into the future.

## Programming paradigms

- Parallel computing paradigms
- Machine learning paradigms

## 1. Files Included

-   [**`final_models.RData`**](./final_models.RData): LASSO models for all three tasks.
-   [**`processed_data.rds`**](./processed_data.rds): Reference data structure.
-   [**`predict_function.rds`**](./predict_function.rds): Helper function for predictions.
-   [**`time_info.rds`**](./time_info.rds): Time information and RMSE values.

## 2. Performance Metrics (RMSE)

-   **Country predictions**: 7.55
-   **Disease predictions**: 7.21
-   **Phase predictions**: 7.91

## 3. Data Timeframe

-   **Last date in training**: `2024-12-28`
-   **Models are suitable for 3-year ahead predictions**.

## 4. Usage Example

``` r 
# Load models and functions load('final_models.RData') predict_fn \<- readRDS('predict_function.rds') time_info \<- readRDS('time_info.rds')

# Generate future time points (36 months)

future_points <- (time_info$last_month + 1):(time_info$last_month + 36)

# Make predictions for any category

predictions <- predict_fn(model, future_points)
