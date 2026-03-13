# Stock Price Movement Prediction using Machine Learning

## Project Overview
This project uses machine learning techniques to predict whether a stock price will move **up or down on the next trading day** based on historical market data and technical indicators.

## Objective
The goal of this project is to analyze historical stock data, engineer useful financial indicators, and train machine learning models to predict the **direction of future stock price movement**.

## Dataset
The dataset contains historical stock market data including:

- Open price
- High price
- Low price
- Close price
- Trading volume

From these values, additional technical indicators were created to improve prediction capability.

## Feature Engineering

The following technical indicators were used as input features:

| Feature | Description |
|------|------|
| MA10 | 10-day moving average of closing price. |
| MA20 | 20-day moving average of closing price. |
| MA50 | 50-day moving average of closing price. |
| EMA12 | 12-day exponential moving average giving more weight to recent prices. |
| EMA26 | 26-day exponential moving average used for trend analysis. |
| MACD | Difference between EMA12 and EMA26 used to detect momentum changes. |
| Daily_Return | Percentage change in closing price from the previous day. |
| Momentum_5 | Difference between current price and price 5 days earlier. |
| Volatility_10 | Standard deviation of returns over the last 10 days representing price volatility. |
| Volume_Change | Percentage change in trading volume from the previous day. |
| HL_Spread | Difference between daily high and low price showing intraday price range. |
| Close_lag1 | Closing price from the previous day. |
| Close_lag2 | Closing price from two days before. |
| Return_lag1 | Daily return from the previous day. |
| Return_lag2 | Daily return from two days before. |

### Target Variable

| Target | Description |
|------|------|
| Target | Binary value representing stock movement: **1 = price increases next day, 0 = price decreases next day** |

## Machine Learning Models Used

Three models were trained and evaluated:

- Logistic Regression
- Linear Regression
- Random Forest

## Model Evaluation

Models were evaluated using:

- Accuracy
- Confusion Matrix
- Precision
- Recall
- F1 Score

## Visualizations Included

The notebook contains several visualizations for better understanding of the data and model performance:

- Stock closing price trend
- Trading volume over time
- Distribution of stock returns
- Moving averages vs price
- Feature importance analysis
- Confusion matrix
- Actual vs predicted stock movement

## Results

All models achieved an accuracy of approximately **51%**, indicating a weak but non-random predictive signal. Logistic Regression performed slightly better compared to Linear Regression and Random Forest.

## Conclusion

Predicting daily stock price movement is challenging due to the complex and unpredictable nature of financial markets. While the models showed limited predictive power, the project demonstrates how machine learning techniques can be applied to financial time-series data.

## Future Improvements

Possible improvements include:

- Using additional technical indicators
- Incorporating sentiment analysis from financial news
- Applying deep learning models
- Using longer historical windows for feature generation
