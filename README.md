# Indian Power Market Analysis

## About the Project

This project analyzes electricity market data from the Indian Energy Exchange (IEX) Real-Time Market.

The main aim is to understand how electricity prices and bidding volumes change during the day and across different trading dates. SQL Server is used for storing and analyzing the data, and Power BI is used for visualization.

## Tools Used

* SQL Server
* Power BI
* DAX
* Power Query

## Dataset

The data used in this project is taken from the IEX Real-Time Market.

The dataset contains information such as:

* Purchase Bid
* Sell Bid
* Market Cleared Volume (MCV)
* Final Scheduled Volume
* Market Clearing Price (MCP)
* Weighted Market Clearing Price
* 15-minute time blocks

The current dataset contains daily data from **24 September 2026 to 1 October 2026**, along with 15-minute data for 1 October 2026.

## What I Analyzed

Using SQL, I analyzed:

* Daily purchase and sell bids
* Market cleared volume
* Daily MCP and weighted MCP
* Purchase-to-sell bid ratio
* Bid imbalance
* Highest MCP days
* Highest-priced time blocks
* Hourly market activity

The results are then used in Power BI to create measures and visualizations.

## Power BI Dashboard

The dashboard is designed to look at the market from a few different perspectives.

### Market Overview

This section focuses on the main market figures:

* Average MCP
* Weighted Average MCP
* Purchase Bids
* Sell Bids
* Market Cleared Volume
* Purchase/Sell Ratio

### Intraday Price Analysis

This section looks at how the Market Clearing Price changes across the 15-minute time blocks and helps identify periods with relatively high or low prices.

### Bid Pressure Analysis

Purchase and sell bids are compared to understand the bidding pattern during different periods of the day.

### Market Volume Analysis

This section tracks Market Cleared Volume and Final Scheduled Volume across different dates and time periods.

## SQL Analysis

The SQL scripts include queries for:

* Daily market summary
* Highest MCP days
* Purchase vs Sell pressure
* Hourly analysis
* Top price time blocks
* Price ranking using window functions

The database contains two main tables:

`Fact_RTM_Daily`

`Fact_RTM_15Min`

## Key Calculations

### Bid Imbalance

```text
Purchase Bids - Sell Bids
```

This shows the difference between purchase and sell bids.

### Purchase/Sell Ratio

```text
Purchase Bids / Sell Bids
```

This is used to compare the relative size of purchase and sell bids.

### MCP Spread

```text
Maximum MCP - Minimum MCP
```

This shows the difference between the highest and lowest Market Clearing Price during the selected period.

## Project Structure

### Data

`data/IEX_RTM_Daily_Current.csv`

`data/IEX_RTM_15Min_2026-10-01.csv`

`data/Data_Dictionary.csv`

`data/validation_summary.csv`

### SQL

`sql/01_Create_Load_and_Analysis.sql`

`sql/02_Refresh_Template.sql`

### Power BI

`powerbi/PowerQuery_SQL_Daily.m`

`powerbi/PowerQuery_SQL_15Min.m`

`powerbi/DAX_Measures.txt`

### Documentation

`docs/PowerBI_Dashboard_Guide.md`

`docs/Current_Market_Observations.md`

## What I Learned

Through this project, I worked with SQL queries involving aggregation, grouping, ratios and window functions.

I also used Power BI and DAX to create metrics and visualizations from the SQL data.

The project gave me an idea of how real market data can be structured and analyzed to understand changes in prices, bidding activity and cleared volumes.

## Data Source

Indian Energy Exchange (IEX) – Real-Time Market

The data used in this project is based on publicly available information from IEX.

## Skills

SQL | SQL Server | Power BI | DAX | Power Query | Data Analysis | Data Visualization
