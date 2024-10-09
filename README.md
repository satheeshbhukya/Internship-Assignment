# Stock Price Prediction using SARIMA

This repository contains a project that forecasts stock prices using the **Seasonal ARIMA (SARIMA)** model. The model is fine-tuned to minimize the Mean Squared Error (MSE) and Mean Absolute Error (MAE) using various hyperparameter tuning techniques.

## Project Overview

The main goal of this project is to predict future stock prices based on historical data. The project implements a **SARIMA** model, a variant of the ARIMA model that incorporates seasonality, to make time series forecasts.

### Key Features:
- Data preprocessing, including handling missing values and differencing for stationarity.
- Hyperparameter tuning for ARIMA and SARIMA models using a grid search approach.
- Model evaluation using MSE and MAE as performance metrics.
- Visualization of train-test split and forecasted results.

## Dataset

The dataset used for this project contains historical stock prices. The data consists of the following columns:
- `Date`: The date of the stock price.
- `Close`: The closing price of the stock for each day.

Make sure your dataset has no missing values in the `Close` column or handle them appropriately before running the model.

## Model

The model used is a **SARIMA (Seasonal AutoRegressive Integrated Moving Average)**. This model is an extension of ARIMA, specifically designed for data with seasonal patterns. The parameters for SARIMA are:
- `(p, d, q)` for the ARIMA component.
- `(P, D, Q, m)` for the seasonal component, where `m` is the length of the seasonality.

### Model Selection and Evaluation

The model's performance is evaluated using:
- **MSE (Mean Squared Error)**
- **MAE (Mean Absolute Error)**
  
These metrics help in selecting the best model by tuning the SARIMA hyperparameters `(p, d, q)` and seasonal orders `(P, D, Q, m)`.

### Hyperparameter Tuning

Grid search is used to find the best combination of parameters that minimize the MSE:
- **p**: AutoRegressive term
- **d**: Differencing term
- **q**: Moving Average term
- **P, D, Q**: Seasonal ARIMA parameters
- **m**: The length of the seasonality

## Requirements

Install the required Python libraries using the following command:

```bash
pip install -r requirements.txt


