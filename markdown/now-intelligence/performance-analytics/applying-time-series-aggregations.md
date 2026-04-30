---
title: Applying time series aggregations
description: You can aggregate changes in indicators into discrete time intervals. These aggregations can make trends more easily visible, or help track progress against a target.Performance Analytics offers four different types of time series. Understand their use cases to know which type to use.The frequency with which scores are collected for the indicator determines which time series are applicable. Some time series include data from partial collection periods.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Applying time series aggregations

You can aggregate changes in indicators into discrete time intervals. These aggregations can make trends more easily visible, or help track progress against a target.

A time series aggregation consists of a math function, such as AVG or SUM, combined with a time formula, such as By quarter. In Platform Analytics, you can select an aggregation when exploring an indicator in [KPI Details](../../par-for-workspace/task/select-time-series-aggregation.md) or when creating a data visualization for an indicator data source, such as a [time series visualization](../../reporting/reference/config-dv-time-series-ind-data.md). In the Core UI, you can select an aggregation either in the [Analytics Hub](scorecard-overview-tab.md#) or when creating a Performance Analytics widget such as a [score widget](../task/create-latest-score-widget.md).

To understand time series aggregations, first consider a watch, phone, or fitness tracker that keeps tabs on how many steps they walked each day. These devices all collect and save your measurements on a minute by minute basis. However, the apps and reports are often designed to show how your activity is progressing compared to last week, last month, or last year. It’s one thing to see if you were more active at noon versus 10 am. What you really want to know, however, is whether you’re continuing to improve over time. Aggregating your steps into weekly, monthly, and yearly scores gives you an easier way to identify trends in your activity.

While daily indicator scores are foundational and almost always desired, sometimes you also want to have the scores available by week, month, or quarter. In other cases, you want to have a month/quarter/year-to-date number that shows cumulative progress up until the current point. Instead of defining multiple indicator sources and indicators to track each interval, Performance Analytics natively allows you to capture the data once and then adjust the view. Use a time series aggregation for any of these scenarios:

-   Aggregate the data to a less frequent period with a Period time series.
-   Smooth out spikes in the data to reveal trends with a Running time series.
-   Determine a period-to-date cumulative score with a To date time series.

**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget or Analytics Hub entry for an indicator that uses such a calendar.

For examples and a deeper exploration of using time series aggregations with indicators, see this Performance Analytics Academy video, [Leveraging Time Series with Performance Analytics](https://youtu.be/aM6JtUndRYk).

## Partial periods

Some time series include indicator scores from incomplete collection periods. These periods can include the current period and the period from the beginning of data collection. A plus sign in the name, +, identifies these time series.

A time series that does not include data from partial periods must have data from the beginning and the end of the period. For example, a **By month SUM** time series aggregation requires scores from the start and the end of the month to be present. Otherwise that month is not included. A time series that includes data from partial periods, such as **By month SUM +**, needs only data from one day in the period.

**Warning:** Partial periods can skew the results of certain aggregations, such as averages.

## Aggregation definitions

Performance Analytics comes with default SUM, AVG, and other time series aggregation definitions.

**Danger**

Do not alter these definitions. Do not add new definitions. Any changes to aggregation definitions can have unexpected results. Creating a new definition can prevent the data collector jobs from running.

## Disallowed time series aggregations

You are not allowed to put a SUM aggregation on an indicator with percentage % as the unit. It is not meaningful to sum percentages.

## Validation of time series aggregations

Time series aggregations are validated on the Analytics Hub and in KPI Details but not in widgets. Therefore, you might navigate from a working widget to the Analytics Hub and get a warning that the indicator has an invalid aggregation.

## Excluding time series aggregations for an indicator

Some time series aggregations, while technically allowed, are not helpful to apply to an indicator. For example, a SUM of percentage values is unlikely to provide useful insight. You can exclude these time series aggregations from the indicator. For more information, see [Exclude time series from an indicator](c_ExcludingTimeSeriesFromIndicators.md).

## Displaying time series aggregations with a date range selector

If on a widget you combine a time series aggregation such as By month SUM with a date range selector, you may show one more time period than you expect. The reason is that when a period such as 3m is selected in the date range selector, the instance interprets that as 0-3 months and shows four months of scores.

**Parent Topic:**[Configure Performance Analytics fundamentals](c_PAWidgetsAndDashboards.md)

**Related topics**  


[Applying time series to result or to contributing indicators](apply-time-series-result-components.md)

[Select time aggregation in KPI Details](../../par-for-workspace/task/select-time-series-aggregation.md)

[Time-series aggregations in the Analytics Hub](scorecard-overview-tab.md#)

[Indicator data options for time series data visualizations](../../reporting/reference/config-dv-time-series-ind-data.md)

[Create a latest score visualization for a score widget](../task/create-latest-score-widget.md)

## Use cases for time series aggregations

Performance Analytics offers four different types of time series. Understand their use cases to know which type to use.

Rounded calculations based on averages may be off by a small amount due to rounding errors.

<table id="table_l1t_gbn_f3b"><thead><tr><th>

Type

</th><th>

Examples

</th><th>

Use Case

</th></tr></thead><tbody><tr><td>

Running

</td><td>

28d running AVG/SUM

 30d running AVG/SUM

 7d running AVG/SUM

 12m running AVG/SUM

 3m running AVG/SUM

 6m running AVG/SUM

 13w running AVG/SUM

 4w running AVG/SUM

 4q running AVG/SUM

</td><td>

Smooths out spikes in the data to make trends easier to spot. For example, looking at daily incident counts may show a drop every weekend, but a 7-day running average smooths out those drops.

</td></tr><tr><td>

To Date

</td><td>

Fiscal quarter-to-date AVG/SUM

 Fiscal year-to-date AVG/SUM

 Month-to-date AVG/SUM

 Quarter-to-date AVG/SUM

 Week-to-date AVG/SUM

 Year-to-date AVG/SUM

</td><td>

Shows cumulative scores for the period. These time series aggregations are very useful if you have a monthly target to hit, but you need to also see the velocity throughout the month.

</td></tr><tr><td>

By Period

</td><td>

By week AVG/SUM

 By month AVG/SUM

 By fiscal quarter AVG/SUM

 By quarter AVG/SUM

 By fiscal year AVG/SUM

 By year AVG/SUM

</td><td>

Shows the cumulative scores for entire periods. While you may want to track the number of P1 incidents daily, the frequency is too high when scores are considered daily. Instead, you can set a target at the monthly level with a "By Month” time series. The current period will never appear in the results because it is incomplete.

</td></tr><tr><td>

By Period \(Including Partial\)

</td><td>

By week + AVG/SUM

 By month + AVG/SUM

 By fiscal quarter + AVG/SUM

 By quarter + AVG/SUM

 By fiscal year + AVG/SUM

 By year + AVG/SUM

</td><td>

The “+” version of the “By” Time Series includes partial periods, so a score is always provided for the current period.

</td></tr></tbody>
</table>## Indicator frequency limitations on time series aggregations

The frequency with which scores are collected for the indicator determines which time series are applicable. Some time series include data from partial collection periods.

When you select a time series aggregation, the frequency with which indicator scores are collected limits which time series you can choose. You cannot select a time series aggregation that is applied to scores more frequently than those scores are collected. For example, the **By week SUM** time series aggregation can apply to an indicator with a daily frequency. However, **By week SUM** cannot apply to an indicator with a weekly, monthly, quarterly, or yearly frequency.

**Note:**

-   Only weekly indicators support the **4w running** and **13w running** time series. Weekly indicators support only weekly and yearly time series.
-   Bi-monthly and yearly indicators do not support any time series aggregations.

The following table shows which time series are supported for which indicator frequencies. These relationships are independent of which aggregation \(AVG, SUM, or custom\) is combined with a time series, and therefore only the time series are shown.

|Time series|Indicator frequencies|
|Daily|Weekly|Monthly|Quarterly \(Fiscal Q, 4-weekly, Bi-weekly\)|
|-----------|---------------------|
|-----|------|-------|-------------------------------------------|
|Daily|Yes|No|No|No|
|7d running|Yes|No|No|No|
|28d running|Yes|No|No|No|
|30d running|Yes|No|No|No|
|4w running|No|Yes|No|No|
|13w running|No|Yes|No|No|
|3m running|No|No|Yes|No|
|6m running|No|No|Yes|No|
|12m running|No|No|Yes|No|
|4q running|No|No|No|Yes|
|By week, by week +|Yes|No|No|No|
|By month, by month +|Yes|No|No|No|
|By quarter, by fiscal quarter, by quarter +, by fiscal quarter +|Yes|No|Yes|No|
|By year, by fiscal year, by year +, by fiscal year +|Yes|Yes|Yes|Yes|
|Week to date|Yes|No|No|No|
|Month to date|Yes|No|No|No|
|Quarter to date, fiscal quarter to date|Yes|No|Yes|No|
|Year to date, fiscal year to date|Yes|Yes|Yes|Yes|

