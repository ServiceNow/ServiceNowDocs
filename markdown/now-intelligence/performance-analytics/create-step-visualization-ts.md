---
title: Create a step visualization for a time series widget
description: To emphasize changes in indicator scores between discreet points in time, create a time series widget with a step visualization.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Time series widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a step visualization for a time series widget

To emphasize changes in indicator scores between discreet points in time, create a time series widget with a step visualization.

## Before you begin

Role required: pa\_power\_user or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

Consider using a step visualization in the following circumstances:

-   You want to emphasize the change in an indicator score between specific points in time, instead of the trend over time.
-   The changes in indicator scores are too small to be easily seen in a line visualization.

The use case for a step visualization is the opposite of the use case for the spline visualization. Use a spline to emphasize a trend or the fuzziness of your data over time.

![A step visualization of a time series with small changes](../image/step-time-series.png "Step visualization - time series")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets** and click **New**.

2.  In the **Name** field, give the widget a name that reflects the information being displayed.

3.  In the **Type** field, select **Time series**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

4.  In the **Visualization** field, select **Step**.

5.  In the **Indicator** field, select the main indicator for which you want to show scores.

6.  Fill in any of the following fields:

<table id="choicetable_b4t_l1p_r1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="choption_first-breakdown"><td>

Breakdown and Element

</td><td>

Only the scores that match the specified element of this breakdown are shown. Select values for both **Breakdown** and **Element**. Otherwise, only scores that are not associated with any element of the breakdown are shown. **Note:** Instead of specifying an element for the first-level breakdown, you can specify an elements filter in the **Elements Settings** tab. Use elements filters for creating personal visualizations. For more information, see [Additional settings for time series widgets](../reference/optional-settings-ts-widgets.md#).

 **Important:** If the widget is for a formula indicator, all contributing indicators in the formula must support the breakdown. Otherwise an error message instead of a value appears in the widget on a dashboard.

</td></tr><tr id="step_second-breakdown"><td>

2nd Breakdown and Element

</td><td>

Drill down to a second level of breakdown and element, if a first-level breakdown and element have been specified. **Note:**

-   Second-level breakdowns must be enabled on the indicator record, in the **Collect breakdown matrix** tab.
-   **Follow element** must be disabled. Dashboard breakdowns count as one breakdown level of the two that are possible.


</td></tr><tr id="step_aggregator"><td>

Time series

</td><td>

Runs a function on the indicator scores for a specific time period, such as a 7-day sum or average. For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget for an indicator that uses such a calendar.

</td></tr><tr id="step_previous-period-chart"><td>

Previous period chart

</td><td>

Compares the scores of the main indicator in similar periods. The **Column** visualization works well for previous period charts. Also consider setting a **Color scheme**.

 Activating Previous Period Chart disables any secondary Widget Indicators.

</td></tr><tr id="step_label"><td>

Label

</td><td>

Specifies a custom label for the main indicator.

</td></tr><tr id="step_color"><td>

Color

</td><td>

A single color that applies only to the scores for the main indicator. This field overrides any color selected in **Color scheme**.

</td></tr><tr id="choption_color-scheme"><td>

Color scheme

</td><td>

A spectrum of colors for the scores for all indicators. If only one indicator is shown, only the first color is used. If you do not specify a color scheme, the default color scheme defined by the **glide.ui.chart.default.colors** property applies.

 You can create your own color scheme instead of using a provided color scheme. For more information, see [Create a color scheme](../concept/color-schemes-pa-widgets.md#).

</td></tr></tbody>
</table>7.  To have the widget follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

        Selecting this option removes the ability to set a second breakdown and element on the widget.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to display separate values for the elements of the Assigned to breakdown. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    3.  In **Show multiple elements as**, select whether to show each element separately or to show an aggregate of elements based on the indicator aggregation.

        Neither all widget visualizations nor all indicators support both aggregate and separate views. For automated and external indicators, only COUNT, SUM, MAX, and MIN data aggregations support aggregate views. COUNT DISTINCT and AVG do not. For more information, see [Showing multiple elements separately or aggregated](../../dashboards/concept/multi-element-select-indicator-views.md).

    **Important:** Do not specify a breakdown and element on the widget record when you want the elements for that breakdown to be selected on a breakdown dashboard. The element on the widget record overrides any elements selected on the breakdown dashboard for that breakdown.

8.  Review the **Settings** tabs and change settings as desired.

    For more information, see [Additional settings for time series widgets](../reference/optional-settings-ts-widgets.md#)

9.  Click **Submit**.


## What to do next

To view the widget, add it to a dashboard or a portal.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[Considerations when creating a time series widget](../concept/considerations-creating-time-series.md)

