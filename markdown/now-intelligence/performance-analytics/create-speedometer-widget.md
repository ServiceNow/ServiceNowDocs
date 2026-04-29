---
title: Create a speedometer or a dial visualization for a score widget
description: To show the latest score of an indicator compared to the range of scores, use a speedometer or dial visualization in a score widget. A speedometer also shows the indicator target.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Score widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a speedometer or a dial visualization for a score widget

To show the latest score of an indicator compared to the range of scores, use a speedometer or dial visualization in a score widget. A speedometer also shows the indicator target.

## Before you begin

Role required: pa\_admin or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is deprecated, meaning it is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

A speedometer visualization shows the latest score with a needle on a speedometer. A dial visualization shows the latest score with a colored in section of a half-circle. By default, the speedometer or dial shows the range of possible scores, but you can create your own range.

The speedometer is particularly useful when a target is set on the indicator. If a direction is set on the indicator \(minimize or maximize\), the visualization reproduces the target and the 3- or 5-color traffic light set on the indicator. For example, the following speedometer shows the Average age open incidents indicator with a Minimize direction, a target of 10, and a 3-color traffic light.

To create a target color scheme, see [Indicator targets](../concept/pa-targets.md#).

![Speedometer of the average age of open incidents with a target of 10 and a three color traffic light. Ten to 11 is yellow and more than11 is red.](../image/speedometer-score-widget.png "Speedometer visualization - score widget")

The dial visualization does not show the indicator [target](../concept/performance-analytics-glossary.md#).

![Dial visualization of the latest score of average age of open incidents](../image/dial-score-widget.png "Dial visualization - score widget")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets** and click **New**.

2.  In the **Name** field, give the widget a name that reflects the information being displayed.

3.  In the **Type** field, select **Score**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

4.  In the **Visualization** field, select **Speedometer** or **Dial**.

5.  In the **Indicator** field, select the indicator for which you want to show scores.

6.  Fill in any of the following fields:

<table id="table_k4q_fhr_w2b"><thead><tr><th>

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
</table>7.  To have the widget follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

        Selecting this option removes the ability to set a second breakdown and element on the widget.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to display separate values for the elements of the Assigned to breakdown. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    **Note:** If multiple elements are selected on the breakdown dashboard, only the aggregate value of the elements can be shown.

    For more information, see [Configure widgets for breakdown dashboards](set-up-widgets-for-breakdown-dashboards.md).

8.  In the **Speedometer/Dial Settings** tab, either select Auto scale, which shows the range of actual scores on the speedometer, or specify another scale.

9.  In the **Element Settings** tab, you can select an element filter instead of selecting a specific element in the **Element** field.

    Use this approach to personalize which breakdowns are shown depending on the viewer. For more information about using element filters to personalize widgets, see [Personalized visuals](../concept/personalized-visuals.md#).

10. Click **Submit**.


## What to do next

To view the widget, add it to a dashboard or a portal.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[Indicator targets](../concept/pa-targets.md#)

