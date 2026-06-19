# Dashboard Design

## Dashboard Overview

The Live Stock Market Intelligence Dashboard is designed as a four-page Power BI report that supports stock market analysis using interactive filters, KPI cards, trend charts, risk indicators, and company comparison visuals.

The dashboard follows a simple analysis flow:

1. Executive Overview
2. Stock Performance Analysis
3. Risk and Volatility Analysis
4. Company Comparison

## Dashboard Architecture

| Page                         | Purpose                                                  |
| ---------------------------- | -------------------------------------------------------- |
| Executive Overview           | Provides a high-level summary of the selected stock      |
| Stock Performance Analysis   | Analyzes open, close, high, low, and volume trends       |
| Risk and Volatility Analysis | Evaluates daily price range and intraday return behavior |
| Company Comparison           | Compares multiple companies side by side                 |

## Page 1: Executive Overview

### Purpose

The Executive Overview page provides a high-level snapshot of the selected stock. It is designed for quick review of price movement, trading volume, and recent market activity.

### Key Visuals

* Average Close Price KPI
* Highest Price KPI
* Lowest Price KPI
* Total Trading Volume KPI
* Closing Price Trend line chart
* Trading Volume Trend chart
* Recent Stock Price Data table
* Select Ticker slicer
* Rolling Date Window slicer

### Business Question Answered

How is the selected stock performing overall during the selected rolling period?

## Page 2: Stock Performance Analysis

### Purpose

The Stock Performance Analysis page provides a deeper view of daily stock movement by comparing open, close, high, low, and volume trends.

### Key Visuals

* Average Open Price KPI
* Average Close Price KPI
* Highest Trading Price KPI
* Lowest Trading Price KPI
* Open vs Close Price Trend
* Daily High vs Low Price Range
* Trading Volume by Date
* Daily Stock Performance Details table
* Select Ticker slicer
* Rolling Date Window slicer

### Business Question Answered

How did the selected stock perform over time based on price and volume movement?

## Page 3: Risk and Volatility Analysis

### Purpose

The Risk and Volatility Analysis page focuses on daily price movement, return behavior, and volatility indicators for the selected stock.

### Key Visuals

* Average Daily Price Range KPI
* Maximum Daily Price Range KPI
* Best Intraday Return % KPI
* Worst Intraday Return % KPI
* Daily Price Range Trend
* Intraday Return % by Date
* Daily Risk and Return Details table
* Select Ticker slicer
* Rolling Date Window slicer

### Business Question Answered

How much risk or volatility does the selected stock show during the selected period?

## Page 4: Company Comparison

### Purpose

The Company Comparison page compares selected technology stocks side by side. It helps users evaluate price trends, trading volume, return movement, and risk indicators across companies.

### Companies Included

* AAPL
* AMZN
* MSFT
* NVDA
* TSLA

### Key Visuals

* Average Close Price KPI
* Highest Price KPI
* Average Daily Price Range KPI
* Total Trading Volume KPI
* Closing Price Trend by Company
* Average Close Price by Company
* Total Trading Volume by Company
* Company Performance Summary table
* Select Companies slicer
* Rolling Date Window slicer

### Business Question Answered

How do selected technology companies compare across price performance, trading activity, returns, and risk?

## Slicer Design

### Select Ticker

Used on Pages 1, 2, and 3 to analyze one selected stock at a time.

### Select Companies

Used on Page 4 to compare two or more companies.

### Rolling Date Window

Used across dashboard pages to show a recent rolling period instead of a fixed date range. This helps the dashboard stay updated when new market data becomes available.

## Design Decisions

* Pages 1–3 focus on selected-stock analysis.
* Page 4 focuses on multi-company comparison.
* Detail tables use “Don’t summarize” to show actual daily records.
* KPI cards use aggregations such as average, maximum, minimum, and total.
* Relative date filtering is used to avoid manually updating fixed date ranges.
* The same data source and visual theme are used across pages for consistency.

## Dashboard Story

The dashboard starts with an executive summary, moves into detailed performance analysis, evaluates risk and volatility, and ends with a multi-company comparison. This structure allows users to move from quick insights to deeper analysis and then to broader market comparison.
