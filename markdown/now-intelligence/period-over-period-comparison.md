---
title: Period over period comparison in time series visualizations
description: Period over period comparison overlays several time periods of an indicator on one time series visualization so that you can spot patterns, trends, and anomalies across the periods.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/period-over-period-comparison.html
release: australia
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [period over period, time series, indicator, compare periods]
breadcrumb: [Time series visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Period over period comparison in time series visualizations

Period over period comparison overlays several time periods of an indicator on one time series visualization so that you can spot patterns, trends, and anomalies across the periods.

When you turn on **Compare period over period** in the **Date range** settings of a time series visualization, each period appears as a separate series on the same chart. The periods are aligned by their position within the period, so you can compare, for example, each year's January or each quarter's first month. Without period over period comparison, the visualization shows a single timeline.

**Note:** Period over period comparison is available starting with the Brazil release.

## Requirements

The **Compare period over period** setting is available only when the visualization meets all of the following conditions:

-   The data source is an indicator. Table data sources aren't supported.
-   The visualization is a time series with a single metric and no group by.
-   The **Number of periods** and **Period** settings are configured.
-   The chart type is Area, Line, Spline, or Step. Column and Scatter charts aren't supported.
-   The visualization doesn't use **Show maximum range** or **Set absolute period**.

Dashboard filters don't work with a time series that has period over period comparison turned on.

## When the setting is hidden

The **Compare period over period** setting is hidden, not turned off, in these cases. The visualization then shows a single timeline, and no message appears.

-   The **Period** is Days.
-   The time aggregation unit is the same as the **Period** unit. For example, the time aggregation is By month and the **Period** is Months.
-   The indicator source or the indicator definition uses a business calendar. Standard and Gregorian calendars aren't business calendars.
-   The indicator is a Data snapshots indicator with a business calendar defined in its trend settings.

If you add a business calendar to the indicator source or definition, the visualization reverts to a single timeline on the next display.

## Period units and time aggregation

The **Period** options are Days, Weeks, Months, Quarters, and Years. The options depend on the time aggregation. A period can't be shorter than the time aggregation unit.

|Time aggregation|Available periods|
|----------------|-----------------|
|Daily|Days, Weeks, Months, Quarters, Years|
|By week \(SUM, AVG, or LAST\)|Weeks, Months, Quarters, Years|
|By month \(SUM, AVG, or LAST\)|Months, Quarters, Years|
|By quarter \(SUM, AVG, or LAST\)|Quarters, Years|
|By year \(SUM, AVG, or LAST\)|Years|

If you change the time aggregation to a unit longer than the current **Period**, the **Period** changes automatically to the shortest period that is still available. For example, if the **Period** is Weeks and you change the time aggregation to By month SUM, the **Period** changes to Months.

The Weeks and Quarters options are available for all visualizations that use indicator data and have a **Period** setting, not only for period over period comparison.

## Series labels and axis labels

The legend, the tooltip, and the data table column headers use the same label for each period. The label depends on the **Period** unit.

|Period|Label format|
|------|------------|
|Years|Full year, such as 2026|
|Quarters|Q, quarter number, and year, such as Q2 2026|
|Months|Month abbreviation and year, such as Apr 2026|
|Weeks|W, ISO week number, and year, such as W22 2026|

The x-axis labels reflect the time aggregation, not the **Period**. The x-axis shows the position within each period.

|Period|Time aggregation|X-axis labels|
|------|----------------|-------------|
|Years|Daily|Jan 1, Jan 2, through Dec 31|
|Years|By week|Week 1 through Week 52|
|Years|By month|Jan through Dec|
|Years|By quarter|Q1 through Q4|
|Quarters|Daily|Month 1 Day 1, Month 1 Day 2, and so on|
|Quarters|By week|Week 1 through Week 13|
|Quarters|By month|Month 1 through Month 3|
|Months|Daily|Day 1 through Day 31|
|Months|By week|Week 1 through Week 4|
|Weeks|Daily|Monday through Sunday|

## Settings that aren't available with period over period comparison

When **Compare period over period** is turned on, these settings are hidden or turned off:

-   **Allow change date range**
-   **Show target**
-   **Show forecast**
-   **Show trend**
-   **Show confidence band**
-   **Show comment**
-   **Show filter as separate series**

The **Show threshold** setting remains available.

-   **[Compare periods in a time series visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/compare-periods-time-series.md)**  
Overlay several periods of an indicator on one time series visualization to compare the same point in each period.

**Parent Topic:**[Create time series data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/create-dv-time-series-ac.md)

