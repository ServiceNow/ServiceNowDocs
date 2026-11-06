---
title: Compare periods in a time series visualization
description: Overlay several periods of an indicator on one time series visualization to compare the same point in each period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/compare-periods-time-series.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
keywords: [period over period, time series, compare periods]
breadcrumb: [Period over period comparison in time series visualizations, Time series visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Compare periods in a time series visualization

Overlay several periods of an indicator on one time series visualization to compare the same point in each period.

## Before you begin

The visualization must be a time series with an indicator data source, a single metric, and no group by. The chart type must be Area, Line, Spline, or Step. For more information, see [Period over period comparison in time series visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/period-over-period-comparison.md).

Role required: admin, or a role that can edit a visualization.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

    Select the time series data visualization you want to edit.

2.  In the metric configuration, select the time aggregation that you want to compare across.

    The time aggregation determines which **Period** options are available.

3.  In the **Date range** section, set the **Number of periods** and the **Period**.

    Leave **Show maximum range** and **Set absolute period** unchecked. Period over period comparison isn't available when either one is on.

4.  Select **Compare period over period**.

    If you don't see this setting, see [Period over period comparison in time series visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/period-over-period-comparison.md) for the conditions that hide it.

    The preview shows each period as a separate series.

5.  Select **Save**.


## Result

The legend, tooltip, and data table column headers show one label for each period, such as 2026 or Q2 2026. The x-axis shows the position within each period.

**Parent Topic:**[Period over period comparison in time series visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/period-over-period-comparison.md)

