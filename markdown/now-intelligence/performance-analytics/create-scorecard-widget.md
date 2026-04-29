---
title: Create a scorecard visualization for a breakdown widget
description: To show the trend for the elements of one breakdown applied to one indicator, use a scorecard visualization.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Breakdown widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a scorecard visualization for a breakdown widget

To show the trend for the elements of one breakdown applied to one indicator, use a scorecard visualization.

## Before you begin

Role required: pa\_admin or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is deprecated, meaning it is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

Scorecard visualizations show the trends by element for one breakdown applied to one indicator.

![Scorecard visualization of the Open incidents indicator split up by the Priority breakdown](../image/scorecard-breakdown.png "Scorecard visualization - breakdown")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets** and click **New**.

2.  In the **Name** field, give the widget a name that reflects the information being displayed.

3.  In the **Type** field, select **Breakdown**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

4.  In the **Visualization** field, select **Scorecard**.

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

    4.  Select a breakdown relation in **Followed breakdown relation**.

        The widget displays only the breakdown elements that follow the specified breakdown relation. A related breakdown element must be selected on the breakdown dashboard. Otherwise, the widget does not display any data. For a detailed example, see [Showing breakdown relations on dashboards](../concept/c_ShowBkdwnRltnsWdgts.md).

        **Note:**

        -   You can specify either a followed breakdown or a followed breakdown relation, not both.
        -   Multiple element selection is not supported on a widget that follows a breakdown relation.
    For more information, see [Configure widgets for breakdown dashboards](set-up-widgets-for-breakdown-dashboards.md).

8.  Fill in any of the following fields:

<table id="table_v4d_rms_1kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time series

</td><td>

Run a function on the scores for a specific time period, such as applying a 7-day sum or average. from being applied to the indicator. For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget for an indicator that uses such a calendar.

</td></tr><tr><td>

Sort onSort direction

</td><td>

Sort the data on the **Sort on** attribute. Then select whether to sort in ascending or descending order.**Note:** The system attempts to sort the data based on the scores from the latest collection job. If the latest job did not collect any scores, the **Sort on** setting is ignored.

</td></tr></tbody>
</table>9.  Review the **Settings** tabs and change settings as desired.

10. Click **Submit**.


## What to do next

To view the widget, add it to a dashboard or a portal.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[Additional settings for breakdown widgets](../reference/optional-settings-breakdown-widgets.md)

[Grouping by breakdown and filtering by breakdown](../concept/grouping-filtering-breakdown.md)

[Interacting with breakdown widgets on dashboards](../concept/c_WidgetInteractivity.md)

[Analytics Hub](../concept/c_UsePerformanceAnalyticsScorecards.md)

