#KOSPI trade market sensitivity prediction Bonus Project 

## Overview
This script implements:
- an LSTM-based model to predict KOSPI index excess returns
- the S&P 500 pipeline extention
- includes feature engineering, weighting, volatility constraints, and provides visualizations

## Requirements
- Python 3.8+
- Libraries: pandas, numpy, matplotlib, yfinance, scikit-learn, tensorflow

project uses python library to download data, therefore simple installation is needed

Installation: `pip install pandas numpy matplotlib yfinance scikit-learn tensorflow`

## How to Run
1. Download `kospi-trade-sensetivity.ipynb`
2. Run in your API: `python kospi-trade-sensetivity.ipynb`
3. Outputs: console metrics of evaluation and a 6 plot figures

## Notes
- Seeds have been implemented for proper reproducibility
- Data is fetched live, therefore turn on internet  connection in the notebook.
- Warnings are suppressed! if issues arise, check TensorFlow/Keras versions. (but generally they are not critical)
- Expected runtime ~1-2 minutes.