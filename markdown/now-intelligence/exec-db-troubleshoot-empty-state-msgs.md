---
title: Troubleshooting executive dashboard empty state messages
description: When a visualization can’t render on a dashboard, it is because it either returns no data or the underlying indicator is misconfigured. Tou see an empty-state message indicating that no data is available.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-01"
reading_time_minutes: 1
breadcrumb: [Executive dashboard overview, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Troubleshooting executive dashboard empty state messages

When a visualization can’t render on a dashboard, it is because it either returns no data or the underlying indicator is misconfigured. Tou see an empty-state message indicating that no data is available.

## Insufficient data

![](../image/error-insufficient-data.png)

If the error is due to insufficient data, do the following steps to troubleshoot"

1.  Verify your date range and filter criteria on the dashboard.
2.  Confirm that the underlying data source table \(incidents, changes, and so on\) contains records matching those criteria.
3.  Run the relevant data collection jobs under **Platform Analytics Administration** &gt; **Data Collector Jobs** to ensure that fresh snapshots exist.

## Invalid configuration

![](../image/error-invalid-breakdown.png)

If the error is due to selection of invalid configuration breakdown, do the following steps to troubleshoot:

1.  Select the required dashboard.
2.  Select the required data visualization and view the associated indicators.
3.  Check if the selected breakdown is present in the indicator, which is used as the data source for the visualization.
4.  Select the appropriate/an available breakdown and save the data.
5.  Run the relevant data collection jobs under **Platform Analytics Administration** &gt; **Data Collector Jobs** to ensure that the data is refreshed.

## Indicator non-existent

![](../image/error-indicator-nonexistent.png)

If the error is because the indicator doesn't exist, do the following steps to troubleshoot:

1.  Select the required dashboard.
2.  Select the required data visualization and view the associated indicators.
3.  Check if the indicator, which is used as the data source for the visualization, is active in the system.
4.  If no, activate the respective content pack plugin to activate the indicator.
5.  Alternately, replace the indicator with another indicator, which is active in the system.
6.  Run the relevant data collection jobs under **Platform Analytics Administration** &gt; **Data Collector Jobs** to ensure that the data is refreshed.

