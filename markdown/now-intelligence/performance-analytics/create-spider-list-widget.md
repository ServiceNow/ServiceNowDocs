---
title: Create a spider visualization in a list widget
description: To plot the scores of several indicators, use a spider visualization in a list widget.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [List widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a spider visualization in a list widget

To plot the scores of several indicators, use a spider visualization in a list widget.

## Before you begin

Role required: pa\_power\_user or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

Use this visualization to help compare the scores of several similar indicators.

**Note:** You can compare a maximum of ten indicators in a spider visualization.

![Spider web visualization of several incident indicators](../image/spider-list-widget.png "Spider visualization - list widget")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets**.

2.  Click **New**.

3.  In the **Name** field, give the widget a name that reflects the information being displayed.

4.  In the **Type** field, select **List**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

5.  In the **Visualization** field, select **Spider**.

6.  Select indicators in one of the following ways:

    -   Select a group in the **Indicator Group** field.
    -   Click **Save**, then add widget indicators as described in [Add widget indicators](add-indicators-to-widget.md).
7.  To aggregate the widget data for a specific time period, such as applying a 7-day sum or average, select a function in the **Time series** field.

    **Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget for an indicator that uses such a calendar.

8.  To have the widget follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to display separate values for the elements of the Assigned to breakdown. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    3.  In **Show multiple elements as**, select whether to show each element separately or to show an aggregate of elements based on the indicator aggregation.

        Neither all widget visualizations nor all indicators support both aggregate and separate views. For automated and external indicators, only COUNT, SUM, MAX, and MIN data aggregations support aggregate views. COUNT DISTINCT and AVG do not. For more information, see [Showing multiple elements separately or aggregated](../../dashboards/concept/multi-element-select-indicator-views.md).

9.  Select the attribute on which to sort the data in the **Sort on** field.

10. Filter which indicators to display in the **List Settings** tab.

    |List setting|Description|
    |------------|-----------|
    |Scorecard options|Select **All** indicators, indicators marked **Key**, or **Favorite** indicators.|
    |Page size|Has no effect. The maximum number of indicators is 10.|


## What to do next

To view the widget, add it to a dashboard or a portal.

