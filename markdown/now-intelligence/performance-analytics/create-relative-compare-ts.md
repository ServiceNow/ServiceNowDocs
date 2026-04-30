---
title: Create a relative compare visualization for a time series widget
description: To show how the relative proportions of several indicators change over time, use a relative compare visualization for a time series.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Time series widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a relative compare visualization for a time series widget

To show how the relative proportions of several indicators change over time, use a relative compare visualization for a time series.

## Before you begin

Role required: pa\_power\_user or admin

## About this task

Like a pie chart, a relative compare visualization shows relative proportions between data points, but it can also show how those proportions change over time. Traditional uses of relative compare visualizations are stock charts or population growth trends. When you create a relative compare visualization, it uses a baseline of zero and then shows how the data changes over time.

For example, this visualization shows the change of the total number of open incidents compared to the change in the number of open incidents that were not updated for 5 or more days. When you point to a line, the number of incidents and the percentage change for that day appear. The percentage change shown for a data point is calculated from a baseline of zero, not the previous data point as on most other time series visualizations.

![Visualization comparing the number of open incidents indicator to the Number of open incidents not updated in 5 days indicator](../image/relative-compare-ts.png "Example of a relative compare visualization for a time series")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets**.

2.  Click **New**.

3.  From the **Type** list, select **Times Series**.

4.  From the **Visualization** list, select **Relative Compare**.

5.  Specify which indicators to include in the visualization with one of the following options.

<table id="choicetable_pm3_bj1_kt"><thead><tr><th align="left" id="d58506e125">

Option

</th><th align="left" id="d58506e128">

Note

</th></tr></thead><tbody><tr><td id="d58506e134">

**Indicator group**

</td><td>

If you select an indicator group, you cannot select a single indicator.**Warning:** This option is not currently functional. Specify a single indicator and additional widget indicators.

</td></tr><tr><td id="d58506e146">

**Indicator**

</td><td>

If you select a single indicator, you must manually add additional indicators in the Widget Indicators related list.

</td></tr></tbody>
</table>6.  Fill in any of the following fields:

<table id="choicetable_grd_cdw_1bb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown and Element

</td><td>

Only the scores that match the specified element of this breakdown are shown. Select values for both **Breakdown** and **Element**. Otherwise, only scores that are not associated with any element of the breakdown are shown. **Note:** Instead of specifying an element for the first-level breakdown, you can specify an elements filter in the **Elements Settings** tab. Use elements filters for creating personal visualizations. For more information, see [Additional settings for time series widgets](../reference/optional-settings-ts-widgets.md#).

 **Important:** If the widget is for a formula indicator, all contributing indicators in the formula must support the breakdown. Otherwise an error message instead of a value appears in the widget on a dashboard.

</td></tr><tr><td>

2nd Breakdown and Element

</td><td>

Drill down to a second level of breakdown and element, if a first-level breakdown and element have been specified. **Note:**

-   Second-level breakdowns must be enabled on the indicator record, in the **Collect breakdown matrix** tab.
-   **Follow element** must be disabled. Dashboard breakdowns count as one breakdown level of the two that are possible.


</td></tr><tr><td>

Time series

</td><td>

Runs a function on the indicator scores for a specific time period, such as a 7-day sum or average. For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget for an indicator that uses such a calendar.

</td></tr></tbody>
</table>7.  Right-click the form header and select **Save**.

8.  If you selected a single indicator, add additional indicators in the Widget Indicators related list.

    If you selected an indicator group, additional indicators are not required.

9.  Select the **Show date range selector** check box on the **Date Settings** tab.

    This setting lets users dynamically change the amount of time displayed in the visualization.

10. To have the widget follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

        Selecting this option removes the ability to set a second breakdown and element on the widget.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to display separate values for the elements of the Assigned to breakdown. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    3.  In **Show multiple elements as**, select whether to show each element separately or to show an aggregate of elements based on the indicator aggregation.

        Neither all widget visualizations nor all indicators support both aggregate and separate views. For automated and external indicators, only COUNT, SUM, MAX, and MIN data aggregations support aggregate views. COUNT DISTINCT and AVG do not. For more information, see [Showing multiple elements separately or aggregated](../../dashboards/concept/multi-element-select-indicator-views.md).

    **Important:** Do not specify a breakdown and element on the widget record when you want the elements for that breakdown to be selected on a breakdown dashboard. The element on the widget record overrides any elements selected on the breakdown dashboard for that breakdown.

11. Fill in the other fields, as appropriate.

12. Click **Update**.


## What to do next

To view the widget, add it to a dashboard or a portal.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[Additional settings for time series widgets](../reference/optional-settings-ts-widgets.md#)

[Considerations when creating a time series widget](../concept/considerations-creating-time-series.md)

[Add widget indicators](add-indicators-to-widget.md)

