# DAX Measures and Calculated Fields

## Overview

This project uses calculated fields and aggregations to support stock market analysis in Power BI. The calculations are used to analyze price movement, trading volume, daily price range, and intraday return behavior.

## Main Table

The primary table used in the dashboard is:

```text
Stock_Prices
```

This table contains daily market data for selected stock tickers.

## Fields Used

| Field     | Description                          |
| --------- | ------------------------------------ |
| timestamp | Trading date                         |
| open      | Opening stock price                  |
| high      | Highest price during the trading day |
| low       | Lowest price during the trading day  |
| close     | Closing stock price                  |
| volume    | Trading volume                       |
| Ticker    | Stock ticker symbol                  |

## Calculated Column: Daily Price Range

### Purpose

The Daily Price Range shows how much the stock price moved during a trading day.

### Formula

```DAX
Daily Price Range = 'Stock_Prices'[high] - 'Stock_Prices'[low]
```

### Business Meaning

A higher daily price range means the stock had larger price movement during the day. This can indicate higher volatility.

## Calculated Column: Intraday Return %

### Purpose

The Intraday Return % shows the percentage change from the opening price to the closing price.

### Formula

```DAX
Intraday Return % = 
DIVIDE(
    'Stock_Prices'[close] - 'Stock_Prices'[open],
    'Stock_Prices'[open]
)
```

### Business Meaning

A positive intraday return means the stock closed higher than it opened. A negative intraday return means the stock closed lower than it opened.

## KPI Aggregations Used

| KPI                       | Field             | Aggregation |
| ------------------------- | ----------------- | ----------- |
| Average Close Price       | close             | Average     |
| Highest Price             | high              | Maximum     |
| Lowest Price              | low               | Minimum     |
| Total Trading Volume      | volume            | Sum         |
| Average Open Price        | open              | Average     |
| Average Daily Price Range | Daily Price Range | Average     |
| Maximum Daily Price Range | Daily Price Range | Maximum     |
| Best Intraday Return %    | Intraday Return % | Maximum     |
| Worst Intraday Return %   | Intraday Return % | Minimum     |

## Chart Aggregations Used

| Visual                          | Field             | Aggregation |
| ------------------------------- | ----------------- | ----------- |
| Closing Price Trend             | close             | Average     |
| Trading Volume Trend            | volume            | Sum         |
| Open vs Close Price Trend       | open, close       | Average     |
| Daily High vs Low Price Range   | high, low         | Average     |
| Daily Price Range Trend         | Daily Price Range | Average     |
| Intraday Return % by Date       | Intraday Return % | Average     |
| Average Close Price by Company  | close             | Average     |
| Total Trading Volume by Company | volume            | Sum         |

## Table Visual Settings

For detail tables, fields are set to **Don’t summarize** so that each row shows the actual daily trading record.

The table visuals include:

1. Recent Stock Price Data
2. Daily Stock Performance Details
3. Daily Risk and Return Details
4. Company Performance Summary

## Formatting Rules

| Field             | Format                         |
| ----------------- | ------------------------------ |
| open              | Decimal number, 2 places       |
| high              | Decimal number, 2 places       |
| low               | Decimal number, 2 places       |
| close             | Decimal number, 2 places       |
| Daily Price Range | Decimal number, 2 places       |
| Intraday Return % | Percentage, 2 decimal places   |
| volume            | Whole number / compact display |

## Notes

The calculations in this project are designed to support beginner-friendly financial analysis while still demonstrating practical Power BI skills such as calculated columns, KPI aggregations, trend analysis, and interactive filtering.
