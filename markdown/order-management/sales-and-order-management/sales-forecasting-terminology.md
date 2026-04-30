---
title: Sales Forecasting terminology
description: Use the following list of terms to gain an understanding of Sales Forecasting concepts, components, and configuration.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-03-29"
reading_time_minutes: 2
breadcrumb: [Sales Forecasting, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Sales Forecasting terminology

Use the following list of terms to gain an understanding of Sales Forecasting concepts, components, and configuration.

## Forecast Model

The forecast Model is a framework or method used to predict future sales based on historical data, current sales activities, and other relevant factors. It helps businesses estimate the expected sales figures over a specific period, such as a quarter or year. Only one forecast model, Opportunity Amount Forecast is available to the users. You can view forecast the sales for the current opportunities in the system.

## Forecast Category

The classification of opportunities is based on the level of certainty regarding their closure. The longer a sales prospect progresses along the sales pipeline, the better their chances of converting.  The forecast admin can configure these categories. By default, these six categories are available:

-   Won:  Opportunities that have already been closed and won.​
-   Commit: Opportunities that sales reps are confident will close within the forecast period.​
-   Strong upside:  Opportunities with greatest potential to close but have some minor uncertainty.
-   Upside: Opportunities with potential to close but with lower level of certainty.
-   Pipeline: Opportunities in the early stages of the sales process with uncertainty if they will be closed deals.
-   Omitted:  Opportunities that are excluded from forecast​ due to lack of data.

## Forecast rollup method

The forecast model defines how opportunities within different categories are aggregated into a forecast. ​There are two primary types of rollups: single and cumulative.

When you select Single, this rollup method ensures that each forecast category is represented in its own column, with only the opportunities in that category being included.

|Column Name on Forecast page|Opportunities that roll up to it from a forecast category|
|----------------------------|---------------------------------------------------------|
|Pipeline|Pipeline|
|Upside|Upside|
|Strong Upside|Strong Upside|
|Commit|Commit|
|Won|Won|

When you select Cumulative, this rollup method aggregates forecast categories in a cumulative manner, where each subsequent category includes the opportunities from the previous categories. Each cumulative rollup method aggregates opportunities from higher order forecast categories.

|Column Name on Forecast page|Opportunities that roll up to it from a forecast category|
|----------------------------|---------------------------------------------------------|
|Open pipeline|Pipeline + Upside + Strong Upside + Commit + Won|
|Cumulative Upside|Upside + Strong Upside + Commit + Won|
|Cumulative Strong Upside|Strong Upside + Commit + Won|
|Cumulative Commit|Commit + Won|
|Won|Won|

## Forecast schedule

The forecast schedule fetches all the opportunities in the system and generates the latest forecast data.

## Sales Quota Management

You can assign sales quota targets to sales representatives and managers based on their hierarchy, role, and forecast period.

