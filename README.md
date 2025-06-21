# Stock Prediction Pipeline

This project retrieves and analyzes historical stock data using the [FinancialModelingPrep API](https://site.financialmodelingprep.com/). It calculates technical indicators, runs predictive models, and visualizes forecast results for a given ticker (e.g., Ford).

## Features

- Scrapes monthly historical stock data using FMP API
- Computes technical indicators using `ta`:
  - SMA, EMA, RSI, MACD, Bollinger Bands, OBV, Volatility
- Builds a clean stock DataFrame with lag features
- Runs 3 forecasting models:
  - Linear Regression
  - Random Forest Regressor
  - LSTM (Keras)
- Plots results vs. actuals

## Example Output
Linear Regression RMSE: 0.23
Random Forest RMSE: 0.24
LSTM RMSE: 0.45
Predicted next close price (moving avg 5 days): 11.12

## Visualizations
Side-by-side plots of predicted vs. actual prices for each model.
Exported CSV with full computed indicator dataset.

## Dependencies
pip install pandas numpy ta scikit-learn matplotlib tensorflow requests beautifulsoup4

## Run script
python stock_pipeline.py

## Notes 
Update the API key in the script to your own FMP key.
The script defaults to Ford ('F') but can be changed to any supported ticker.
