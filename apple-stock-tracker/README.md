# Stock Market Analysis & Trend Modeling (Python)

## Overview

This project analyzes historical stock market data to understand price behavior, market trends, momentum, and risk over time. The analysis focuses on Apple’s stock (AAPL) from 2020 to 2025 and combines technical analysis, time-series exploration, risk evaluation, and basic predictive modeling.

The main goal was to explore how stock prices move over time using indicators such as moving averages, Bollinger Bands, RSI, volatility, and trading signals, and then apply statistical and machine learning methods to better understand performance, risk, and market behavior.

## Objectives

* Explore historical stock price trends
* Analyze momentum and volatility using technical indicators
* Identify potential buy and sell signals
* Evaluate risk and performance using financial metrics
* Apply basic predictive modeling to stock price data
* Interpret stock behavior using both technical and fundamental analysis

## Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* yfinance
* Scikit-learn
* statsmodels

## Dataset

This project uses historical stock market data from Yahoo Finance, accessed through the `yfinance` Python library.

* Source: Yahoo Finance
* Ticker used: AAPL
* Date range: 2020-01-01 to 2025-01-01
* Dataset includes variables such as Open, High, Low, Close, Adjusted Close, and Volume

## Project Workflow

### 1. Data Collection & Preprocessing

* Downloaded historical stock price data for Apple using `yfinance`
* Loaded the data into a Pandas DataFrame for analysis
* Prepared the dataset for time-series analysis and visualization
* Converted date values into numeric form when needed for regression modeling

### 2. Trend Analysis

* Calculated the 50-day moving average to capture short-term price trends
* Calculated the 200-day moving average to capture long-term price trends
* Visualized stock price movement alongside moving averages to identify overall trend direction and crossover behavior

### 3. Return & Volatility Analysis

* Calculated daily returns using percentage change in closing price
* Measured rolling volatility using the standard deviation of daily returns
* Used these metrics to understand how much the stock fluctuates over time and to evaluate short-term risk

### 4. Technical Indicators

#### Bollinger Bands

* Calculated upper and lower Bollinger Bands using the 50-day moving average and rolling volatility
* Used Bollinger Bands to highlight periods where the stock may appear relatively overbought or oversold

#### Relative Strength Index (RSI)

* Built a custom RSI function to measure price momentum over a 14-day period
* Used RSI to identify potential momentum-based reversal points and overbought / oversold conditions

### 5. Trading Signal Generation

* Created buy and sell signals using a moving average crossover strategy
* Assigned buy signals when the 50-day moving average moved above the 200-day moving average
* Assigned sell signals when the 50-day moving average moved below the 200-day moving average
* Visualized these signals directly on the stock price chart to show potential entry and exit points

### 6. Predictive Modeling

#### Linear Regression

* Built a linear regression model using time as the input variable and closing price as the target
* Split the data into training and test sets while preserving chronological order
* Compared predicted prices against actual prices to evaluate how well a simple regression model captures stock trends over time

#### Seasonal Decomposition

* Applied seasonal decomposition to separate the stock price series into trend, seasonal, and residual components
* Used a period of 252 trading days to represent a typical trading year
* Explored whether long-term structure or recurring patterns could be observed in the stock data

### 7. Risk & Performance Evaluation

* Calculated the Sharpe Ratio to measure return relative to volatility
* Calculated cumulative returns to show how the stock would have grown over time from an investment perspective
* Calculated maximum drawdown to measure the largest decline from a previous peak
* Created a summary statistics section to capture mean return, volatility, Sharpe ratio, and maximum drawdown in one place

### 8. Fundamental Analysis

* Used `yfinance` to retrieve company financial statement data
* Reviewed financial information such as revenue, expenses, and net income
* Added a fundamental analysis component to complement the technical and statistical analysis

## Key Results

* Identified short-term and long-term stock trends using moving averages
* Measured stock momentum and overbought / oversold conditions using RSI and Bollinger Bands
* Generated rule-based buy and sell signals from moving average crossovers
* Evaluated performance and risk using daily returns, volatility, Sharpe ratio, cumulative returns, and maximum drawdown
* Explored the limitations of simple linear regression for stock prediction
* Added company financial data to provide a broader perspective beyond technical indicators

## Skills Demonstrated

* Data collection using APIs
* Data cleaning and preprocessing
* Time-series analysis
* Technical indicator engineering
* Financial risk analysis
* Data visualization
* Predictive modeling with linear regression
* Trend and seasonal decomposition
* Fundamental stock analysis
* Interpretation of financial metrics and signals

## Files

* `stock_market_analysis.ipynb` – main notebook with stock data collection, technical indicators, modeling, and evaluation
* `README.md` – project overview and documentation

## How to Run

* Open the notebook in Google Colab or Jupyter Notebook
* Install the required libraries if needed
* Run the notebook cells from top to bottom
* Review the charts, technical indicators, predictive modeling outputs, and summary statistics

## Future Improvements

* Compare multiple stocks instead of focusing on one company
* Add benchmark comparisons against the S&P 500
* Use more advanced forecasting models such as ARIMA, Prophet, or LSTM
* Build an interactive dashboard in Tableau, Power BI, or Streamlit
* Backtest trading strategies more formally using portfolio return calculations

## Dataset

This project uses historical stock market data from Yahoo Finance, accessed programmatically through the `yfinance` library.

* Source: Yahoo Finance
* Ticker analyzed: AAPL
* Date range analyzed: 2020-01-01 to 2025-01-01

## Author

Aran Pathmarajah

This project was created as part of my data science portfolio to strengthen my skills in time-series analysis, financial data analysis, predictive modeling, and real-world insight generation.
