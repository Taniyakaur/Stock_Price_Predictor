# Stock_Price_Predictor
# Stock Price Predictor (KNN)

A simple stock price prediction and trading-signal notebook using K-Nearest Neighbors (KNN).  
This project demonstrates:
- A KNN classifier that predicts Buy (+1) / Sell (-1) signals for the next day.
- A KNN regressor that predicts the next day's closing price.
- Basic feature engineering using daily Open/High/Low/Close data fetched via yfinance.

Notebook: Stock Predictor using KNN.ipynb

---

## Table of contents
- Project overview
- What the notebook does
- Requirements
- Quick start
- Key results & known issue
- Suggestions for improvement
- Files in this repo
- License & contact

---

## Project overview
This notebook downloads historical price data for a ticker (DBK.DE in the notebook), computes two features:
- `Open - Close`
- `High - Low`

Then it:
- Builds a classification dataset where the target is +1 if the next day's Close is higher than today (buy), else -1 (sell).
- Trains a KNN classifier (GridSearchCV to pick k) and reports accuracy on train/test splits.
- Builds a regression dataset to predict the next day's Close price, trains a KNN regressor (GridSearchCV), and evaluates predictions with RMSE.

---

## What the notebook does (high level)
1. Downloads historical OHLCV data using yfinance.
2. Creates simple features and the classification/regression targets.
3. Splits data into train/test.
4. Uses GridSearchCV to choose the best `n_neighbors` for both classification and regression.
5. Reports accuracy for the classifier and prints regression predictions and RMSE.
6. Displays comparisons of actual vs predicted values.

---

## Requirements
- Python 3.8+
- Jupyter / JupyterLab (to run the notebook)
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - yfinance
  - scikit-learn

Install with pip:
