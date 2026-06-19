# Data Source

## Data Source Overview

This project uses stock market data retrieved through a web API connection in Power BI. The dashboard is connected to Yahoo Finance web data through Power Query and refreshes market data for selected stock tickers.

## Source Used

The dashboard uses Yahoo Finance web data for daily stock market information.

## Stock Tickers Included

The dashboard analyzes the following companies:

| Ticker | Company               |
| ------ | --------------------- |
| AAPL   | Apple Inc.            |
| AMZN   | Amazon.com Inc.       |
| MSFT   | Microsoft Corporation |
| NVDA   | NVIDIA Corporation    |
| TSLA   | Tesla Inc.            |

## Data Fields Used

The following fields are used in the dashboard:

| Field             | Description                                           |
| ----------------- | ----------------------------------------------------- |
| timestamp         | Trading date                                          |
| open              | Opening stock price for the trading day               |
| high              | Highest stock price during the trading day            |
| low               | Lowest stock price during the trading day             |
| close             | Closing stock price for the trading day               |
| volume            | Number of shares traded                               |
| Ticker            | Stock symbol for the company                          |
| Daily Price Range | Difference between high price and low price           |
| Intraday Return % | Percentage return from opening price to closing price |

## Data Refresh Method

The data is connected through Power Query using a web API connection. When the semantic model is refreshed, Power BI retrieves the latest available market data from the source.

## Date Window

The dashboard uses a rolling date window to show recent market activity. This avoids fixed date filters and helps the dashboard update automatically when new trading data becomes available.

## Data Preparation Steps

The data preparation process includes:

1. Connecting Power BI to the web API source
2. Retrieving daily stock market data for selected tickers
3. Converting Unix timestamp values into readable date format
4. Cleaning null or blank price records
5. Assigning each record to the correct stock ticker
6. Creating calculated fields for price range and intraday return
7. Loading the cleaned data into Power BI for visualization

## Notes

This project is created for portfolio and learning purposes. The dashboard is intended to demonstrate data analysis, Power BI dashboard development, Power Query transformation, and financial market visualization skills.
