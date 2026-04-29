---
title: Select time aggregation in KPI Details
description: You can aggregate changes in indicators into discrete time intervals. A time aggregation consists of an AVG or SUM function combined with a time series, such as By quarter.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Examining indicators, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Select time aggregation in KPI Details

You can aggregate changes in indicators into discrete time intervals. A time aggregation consists of an AVG or SUM function combined with a time series, such as By quarter.

## Before you begin

**Note:** Native Data snapshots indicators do not have time aggregations. Instead, you can select an aggregation period to trend by. For more information, see [Configure trend for a native Data snapshots indicator in KPI Details](configure-trend-ds-indicator.md)

Role required: None. However, upgraded instances may require pa\_viewer.

## About this task

To explore a different time aspect of the indicator, apply one of the following time aggregations:

-   **Running**

    Smooth out spikes to reveal trends. For example, looking at daily incident counts may show a decrease every weekend, but a 7-day running average smooths out those drops.

-   **Period**

    Aggregate data to a less frequent period. For example, you may want to track the number of P1 incidents daily, but the frequency is too high when scores are considered daily. Instead, you can set a target at the monthly level with a "By Month” time series.

-   **To date**

    Show cumulative scores. These time aggregations are useful when you have a monthly target to hit, but you also need to see the velocity throughout the month.


For more information about the use, behavior, and limitations of time aggregations, see [Applying time series aggregations](../../performance-analytics/concept/applying-time-series-aggregations.md#). For examples and a deeper exploration of using time series aggregations with indicators, see this Performance Analytics Academy video, [Leveraging Time Series with Performance Analytics](https://youtu.be/aM6JtUndRYk).

## Procedure

1.  Open KPI Details for an indicator, as described in [View KPI Details](../../performance-analytics/task/view-kpi-details.md).

2.  Expand the time aggregation menu, which has a label matching the currently selected aggregation period, usually Daily.

    ![The control for expanding the time aggregation menu](../image/kpi-details-open-time-aggregate.png)

    **Note:** Time aggregations are not available for real-time scores. When you select a time aggregation, real-time scores are disabled. If you return to the default frequency, real-time scores are re-enabled but turned off. You can turn them on if you want.

3.  Select either a **Running**, a **Period**, or a **To date** aggregation to configure.

4.  Select a time period.

    Invalid and excluded time periods for the indicator frequency are not enabled. For more information about excluded time periods, see [Exclude time series from an indicator](../../performance-analytics/concept/c_ExcludingTimeSeriesFromIndicators.md).

5.  Select either the average or the sum function.

6.  If you have selected a **Period** aggregation, decide whether to **Include partial periods**.

    If you include partial periods, you show a score for the current period even when it has not yet completed. Use caution because including partial periods can skew averages.


## Result

The indicator visualization refreshes with each selection you make. Change your selection as much as you want. To return to the default time aggregation for the indicator, select **Reset**.

## Time aggregation on an daily indicator

In the following time aggregation menu, the daily indicator Number of open incidents is aggregated by period to a weekly sum. Partial weeks are not included.

![Time aggregation menu for a daily indicator, showing a Period aggregation to a weekly sum](../image/kpi-details-time-aggregation.png)

**Parent Topic:**[Examining indicators with KPI Details](../reference/kpi-details-components.md)

**Related topics**  


[View contributing indicators to a formula in KPI Details](../concept/view-formula-components.md)

[Show, compare, create, and edit records in KPI Details](../concept/show-compare-edit-records.md#)

[Chart options in KPI Details](../reference/chart-options.md)

[Configure trend for a native Data snapshots indicator in KPI Details](configure-trend-ds-indicator.md)

[Configure display properties for a Data snapshots indicator](configure-display-properties-ds-indicator.md)

[Filter indicator scores by breakdown elements in KPI Details](apply-brkdowns-element-kpi-details.md#)

[Filter native Data snapshots indicator scores in KPI Details](filter-data-snapshots-indicator-scores.md)

[Access indicator record or scoresheet from KPI Details](access-indicator-record-scoresheet.md)

