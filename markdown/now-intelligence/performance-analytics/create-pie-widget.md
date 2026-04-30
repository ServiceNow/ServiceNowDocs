---
title: Create a pie, donut, or semi-donut visualization for a breakdown widget
description: To show the relative proportions of the elements of a breakdown, use a pie, donut, or semi-donut visualization.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Breakdown widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a pie, donut, or semi-donut visualization for a breakdown widget

To show the relative proportions of the elements of a breakdown, use a pie, donut, or semi-donut visualization.

## Before you begin

Role required: pa\_power\_user or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

When you need to compare the percentages or relative proportions of breakdown elements, you can use a pie, a donut, or a semi-donut visualization. Consider trying all three to see which works best for a particular widget.

These visualizations can be unclear in the following cases:

-   The breakdown has many elements.
-   Several elements in the breakdown are much smaller than the others.

In these cases, or to compare scores instead of proportions, consider using a column visualization.

![Pie visualization applied to open incidents by priority](../image/pie-breakdown.png "Pie, donut, and semi-donut visualizations") ![Donut visualization applied to open incidents by priority](../image/donut-breakdown.png "Pie, donut, and semi-donut visualizations") ![Semi donut visualization applied to open incidents by priority](../image/semi-donut-breakdown.png "Pie, donut, and semi-donut visualizations")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets** and click **New**.

2.  In the **Name** field, give the widget a name that reflects the information being displayed.

3.  In the **Type** field, select **Breakdown**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

4.  In the **Visualization** field, select **Pie**, **Donut**, or **Semi donut**.

    You can let the user switch between visualizations. Select **Show visualization selector** in the **Display settings** tab.

5.  In the **Indicator** field, select the main indicator which you want to break down.

6.  Select the breakdown to group the scores.

    You may also set a breakdown and element to filter the scores.

    -   For the widget to show scores grouped by the elements of a breakdown, select a breakdown in the **Breakdown** field. Do not select an element or a second breakdown.
    -   You can have the widget show different elements depending on characteristics of the viewer. To do so, specify an elements filter in the **Element Settings** tab. Do not specify an element in the **Element** field. You can personalize only the first-level breakdown elements. For more information, see [Personalized visuals](../concept/personalized-visuals.md#).
    -   For the widget to show scores filtered by an element of one breakdown then grouped by the elements of another breakdown, select the filtering breakdown and element in the **Breakdown** and **Element** fields. Then select the grouping breakdown in the **2nd Breakdown** field. The widget shows scores for each element of the **2nd Breakdown** but only if they match the first **Breakdown** and **Element**.

        **Note:**

        -   Second-level breakdowns must be enabled on the indicator record, in the **Collect breakdown matrix** tab.
        -   To have a second breakdown, **Follow element** must be disabled. Dashboard breakdowns count as one breakdown level of the two that are possible.
    -   The widget can also show scores grouped by one breakdown and filtered by an element that the user selects on a breakdown dashboard. Select the grouping breakdown in the **Breakdown** field. Then select **Follow element** as described in a later step.
    **Important:** If the widget is for a formula indicator, all contributing indicators in the formula must support the breakdown. Otherwise an error message instead of a value appears in the widget on a dashboard.

7.  To have the widget follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

        Selecting this option removes the ability to set a filtering breakdown on the widget. Scores are grouped by the elements of the first breakdown and filtered by the elements that the user selects on the dashboard.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to show separate values for the elements of the breakdown Assigned to. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    3.  In **Show multiple elements as**, only the **Aggregated** view is possible.

    For more information, see [Configure widgets for breakdown dashboards](set-up-widgets-for-breakdown-dashboards.md).

    **Note:** The **Followed breakdown relation** menu works only with Scorecard visualizations. Also, multiple element selection on a breakdown dashboard is not supported on the widget when you set a breakdown relation to follow.

8.  Fill in any of the following fields:

<table id="choicetable_kbb_mhw_1bb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="chrow_time-series"><td>

Time series

</td><td>

Run a function on the scores for a specific time period, such as applying a 7-day sum or average. from being applied to the indicator. For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget for an indicator that uses such a calendar.

</td></tr><tr id="chrow_sort-on"><td>

Sort onSort direction

</td><td>

Sort the data on the **Sort on** attribute. Then select whether to sort in ascending or descending order.**Note:** The system attempts to sort the data based on the scores from the latest collection job. If the latest job did not collect any scores, the **Sort on** setting is ignored.

</td></tr><tr><td>

Color scheme

</td><td>

A spectrum of colors for the scores for all breakdowns. If only one breakdown is shown, only the first color is used. If you do not specify a color scheme, the colors defined in the system property **glide.ui.chart.default.colors** apply.

 You can create your own color scheme instead of using a provided color scheme. For more information, see [Create a color scheme](../concept/color-schemes-pa-widgets.md#).

</td></tr></tbody>
</table>9.  Review the **Settings** tabs and change settings as desired.

    For more information, see [Additional settings for breakdown widgets](../reference/optional-settings-breakdown-widgets.md).

10. Click **Submit**.


## What to do next

To view the widget, add it to a dashboard or a portal.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[Grouping by breakdown and filtering by breakdown](../concept/grouping-filtering-breakdown.md)

[Interacting with breakdown widgets on dashboards](../concept/c_WidgetInteractivity.md)

