# Data_exploratory.ipynb

## Overview
This Jupyter notebook contains exploratory data analysis of Apple (AAPL) stock data from 2010 to present. The analysis focuses on historical price trends, visualization, and basic data processing.

## Contents
The notebook includes the following analyses:

1. **Data Acquisition**
   - Fetching Apple stock data using yfinance API
   - Data validation and quality checks

2. **Data Visualization**
   - Historical Open and Close prices visualization
   - Recent 5-year trend analysis
   - Time series plots with proper formatting

3. **Data Processing**
   - Filtering for recent time periods
   - Data integrity verification
   - Saving processed datasets for further analysis

## Requirements
To run this notebook, you need:
- Python 3.x
- pandas
- numpy
- matplotlib
- yfinance
- seaborn


# Install required packages (if needed)
pip install pandas numpy matplotlib yfinance seaborn

# Launch Jupyter Notebook
jupyter notebook Data_exploratory.ipynb
```

## Key Insights
This exploratory analysis helps understand:
- Long-term price trends in Apple stock
- Visualization of key price metrics
- Data preparation for more advanced analyses

## Future Work
Potential extensions to this exploratory analysis include:
- Adding technical indicators
- Performing statistical analysis on returns
- Implementing price prediction models:
  - LSTM (Long Short-Term Memory) neural networks for time series forecasting
  - Linear regression models for trend analysis
- Comparing model performance on training and testing datasets
- Evaluating prediction accuracy using metrics like RMSE and MAE
- Comparing with market indices or other tech stocks