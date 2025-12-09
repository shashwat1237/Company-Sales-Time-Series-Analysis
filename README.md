Kaggle dataset link - https://www.kaggle.com/datasets/podsyp/time-series-starter-dataset
📈 SARIMA Time-Series Forecasting Project

Forecasting monthly revenue using statistical modeling (SARIMAX), stationarity tests, differencing, and model comparison.

📌 Project Overview

This project builds a SARIMA model to forecast monthly revenue data.
It walks through the full pipeline of:

Loading and preparing the dataset

Testing for stationarity

Applying log transforms and differencing

Analyzing ACF/PACF plots

Training a SARIMA model

Comparing performance against a seasonal naïve baseline

Visualizing actual vs. predicted values

The workflow demonstrates real-world time-series forecasting from raw data → model evaluation → forecast visualization.

🗂️ Dataset

File used: Month_Value_1.csv
Contains monthly revenue values.
The goal is to predict future values based on past seasonal and trend patterns.

🧪 Key Steps Explained
1. Import Libraries

Uses pandas, numpy, matplotlib, statsmodels, sklearn — the essentials for time-series analysis.

2. Load Data

Reads the CSV into a DataFrame to begin exploration and modeling.

3. Stationarity Check (ADF Test)

The Augmented Dickey-Fuller test is applied to check if the series is stationary.
Time-series models like ARIMA/SARIMA require stationarity.

4. Differencing

Three forms of differencing are tried:

First difference → removes trend

Seasonal difference → removes yearly seasonality

Combined → stabilizes the series completely

Log transform is also applied to reduce variance.

5. ACF / PACF Plots

Autocorrelation and partial autocorrelation are analyzed to guide SARIMA parameter selection.

6. Train–Test Split

80% of data is used for training, 20% for testing forecasts.

7. SARIMA Model

Model used:

order = (1, 1, 1)
seasonal_order = (1, 1, 1, 12)


Captures both trend & seasonal patterns

Produces 12-step forecasts

Provides confidence intervals

8. Seasonal Naïve Baseline

A simple benchmark model assuming:

Next year’s values = last year’s values

This helps assess whether SARIMA truly improves over a basic baseline.

9. Model Evaluation

Metric used: RMSE (Root Mean Squared Error)

Printed results show whether SARIMA outperforms the naïve model.

10. Visualization

A clean plot comparing:

Actual test values

SARIMA predictions

Naïve seasonal predictions

SARIMA confidence intervals

This reveals how well the model fits and generalizes.

📊 Findings & Insights

Differencing (first + seasonal) made the series stationary.

Log transform helped stabilize variance.

SARIMA model captured both seasonality and trend patterns.

SARIMA achieved lower RMSE than the seasonal naïve model, proving it has better predictive accuracy.

Forecast plot shows smooth, reliable predictions with reasonable uncertainty bounds.

