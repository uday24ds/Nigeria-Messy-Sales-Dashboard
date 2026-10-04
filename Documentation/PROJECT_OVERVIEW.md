# Project Overview

## Business context
This report explores sales performance across products, customers, Nigerian states, sales channels, and time periods using a messy sales dataset.

## Data preparation
The Power Query model includes text trimming and cleaning, capitalization standardization, data type conversion, handling of blank customer/channel labels, and joins to dimension tables. Inspect each transformation and validate the resulting row counts and totals before using the report for decisions.

## Model
The model contains `Fact_Sales` and dimensions for customer, product, state, sales channel, and date. The staging query is named `stg_Sales`.

## Important validation
The current `YOY Sales Growth` measure uses `[Previous Month Sales]` in its calculation. That is a month-over-month calculation, not year-over-year. Update it to compare `[Total Sales]` against `[Previous Year Sales]` if the intended metric is YoY. The `MOM sales growth` measure also compares against previous-month sales, which is appropriate for MoM.

The Power Query staging source currently uses a Windows-specific path. Update it before refreshing the report on another computer.

## Portfolio improvements to consider
- Add a data dictionary and dataset source/license details.
- Document key business questions and verified findings from the dashboard.
- Add a short description of each report page and important slicers/interactions.
- Validate missing values, duplicate order IDs, negative values, and sales arithmetic.
