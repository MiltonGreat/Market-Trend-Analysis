# Market Trend Analysis Using Exponential Smoothing and Prophet

![screenshot-localhost_8888-2025 03 30-16_10_27](https://github.com/user-attachments/assets/0c464028-3a9d-4195-a83d-82b1770c891d)

### Project Overview

This project aims to analyze and forecast stock market trends by utilizing two popular time series forecasting techniques: Exponential Smoothing and Prophet. The goal is to identify underlying market patterns, trends, and seasonal effects to help investors and analysts make informed decisions based on historical data.

### Key Objectives
- Apply Exponential Smoothing (Holt-Winters) to detect seasonal trends and smooth out stock price fluctuations.
- Use Prophet to account for external factors like holidays and changepoints, and make flexible, robust forecasts.
- Visualize the market trends and compare the performance of the two models.

### Dataset

The dataset contains historical stock price data for various companies, with each entry representing a single day of trading. Below is a detailed description of each column in the dataset:

- Ticker: The stock symbol for the company. Each entry in this column represents a different company, such as 'A' for one specific company.
- Date: The date of the stock price data entry, formatted as YYYY-MM-DD. This column helps in organizing the data chronologically, allowing time-based analysis and forecasting.
- Open: The price of the stock at the beginning of the trading day. It represents the price at which the stock first traded when the market opened on that particular day.
- High: The highest price that the stock reached during the trading day. This shows the peak price the stock was sold for on that particular day.
- Low: The lowest price the stock reached during the trading day. This represents the bottom point during the day for the stock price.
- Close: The last price at which the stock was traded during the day. It’s typically used as the reference price for that day and is often the most important data point for financial analysis.
- Adj Close (Adjusted Close): The closing price of the stock adjusted for actions like dividends, stock splits, etc. This is crucial for a more accurate reflection of stock performance, as it accounts for such events that affect stock value but not the market price directly.
- Volume: The total number of shares that were traded on that particular day. This is an important indicator of market activity, showing how much interest or liquidity there is in the stock for that day.

### Project Workflow

1. Data Preparation:
- Stock data for the selected company (e.g., AAL) is loaded and preprocessed.
- The data consists of various columns, including Date and Close price, which is used for trend analysis.

2. Exponential Smoothing (Holt-Winters):
- The Exponential Smoothing method is applied to the Close price data.
- This model captures the underlying trend and seasonal patterns by assuming a combination of trend and seasonality components.
- The seasonal_periods=252 parameter is used to model yearly seasonality (252 trading days per year).

3. Prophet Model:
- The Prophet model is initialized and fitted to the stock data. Prophet is especially useful for handling seasonality and external factors such as holidays.
- The add_country_holidays('US') feature allows for the inclusion of US market holidays, improving the model's accuracy.
- The model is trained to predict the next 30 days of stock prices.

4. Visualization:
- The predictions from both models are plotted for easy comparison.
- The Exponential Smoothing results are compared to actual data in a Holt-Winters plot, while Prophet’s forecast is visualized using its built-in plotting function.

### Results and Insights

- The Exponential Smoothing model provides a smoothed version of stock data, highlighting the trend and seasonal patterns.
- The Prophet model, with the inclusion of holidays, captures the seasonality and trends more effectively, especially in handling abrupt changes in stock prices.
- Visualizing both models allows for easy comparison, showing how they model market trends and forecast future prices.

### Conclusion

By applying Exponential Smoothing and Prophet to stock market data, this project provides an insightful analysis of market trends. Both models offer valuable forecasting capabilities, with Exponential Smoothing focusing on trend and seasonality, and Prophet incorporating external factors like holidays. This analysis can assist in making informed investment decisions and identifying significant trends in the market.

### Future Enhancements

- Explore other time series forecasting models (e.g., ARIMA, LSTM, GRU).
- Implement additional market indicators (e.g., volume, volatility) in the analysis.
- Compare the forecasting performance of multiple models to select the best predictor for stock prices.

### Source

![S&P 500 Stock Data From Listing Day to 2023 from Kaggle](https://www.kaggle.com/datasets/pavankrishnanarne/s-and-p-500-stock-data-from-listing-day-to-2023)


