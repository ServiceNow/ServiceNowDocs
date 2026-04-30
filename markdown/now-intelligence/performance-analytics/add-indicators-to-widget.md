---
title: Add widget indicators
description: Add any number of secondary indicators to an existing time series or list widget.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Add widget indicators

Add any number of secondary indicators to an existing time series or list widget.

## Before you begin

The widget must exist. If you want to add indicators to a widget that you are creating, save the widget instead of submitting it. The form remains open and the Widget Indicators related list appears at the bottom.

Role required: pa\_power\_user or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

When you create a time series widget, you associate it with a single, main indicator. If you want to compare this indicator to another indicator in the same widget, add the additional indicator to the existing widget. This procedure is necessary when you create a Stacked Column visualization for a time series.

When you create a list widget, you must either specify an indicator group or add widget indicators.

**Note:** When you include main and widget indicators with different frequencies on a time series widget, be aware of how the widget shows time values on the x-axis. For more information about this behavior, see [KB0755757](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3D9ff78fc4dbc7b38823f4a345ca9619b9).

If the widget follows elements on a breakdown dashboard, the **Show multiple elements as** value applies to both the main widget and any widget indicators. If **Aggregate** is selected but one of the widget indicators does not support the **Aggregate** view, that indicator does not follow the elements on the breakdown dashboard. Instead, the indicator follows any first-level breakdown and element that are set in the widget configuration. The other indicators follow the elements on the breakdown dashboard and show an aggregate of their values. For more information, see [Configure widgets for breakdown dashboards](set-up-widgets-for-breakdown-dashboards.md).

**Warning:** You cannot have Previous Period Chart and widget indicators on the same time series widget. If you enable Previous Period Chart on a time series that already has widget indicators specified, the widget indicator list is cleared.

When a user selects breakdown elements on a breakdown dashboard, the breakdown and element names are appended to the widget indicator names. Widget indicator labels also have the breakdown and element names appended. The breakdown and element names are not appended to the widget indicator names and labels in the following circumstances:

-   The widget shows an aggregate view of multiple elements, and the widget indicator does not support this view.
-   The widget does not follow elements.
-   The widget indicators do not support the selected breakdown elements.

## Procedure

1.  Either save a widget that you are creating, or open an existing widget for editing.

    You can open a widget either from **Performance Analytics** &gt; **Widgets** or from the dashboard. For more information, see [Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md).

2.  Scroll to the bottom of the form and locate a related list with the label **Widget Indicators**.

3.  Click **New**.

4.  In the **Indicator** field, select a secondary indicator for the widget.

    Selecting too many indicators might make your widget difficult to read.

5.  In the **Chart type** field, select a visualization for the indicator.

    Select a visualization that works well with the visualization of the primary indicator. For instance, show the primary indicator as columns and the secondary indicators as lines. If you are using a **Stacked Column** visualization for the primary indicator of a time series widget, set all secondary indicators to also use **Stacked Column**.

6.  Fill in any of the following fields:

<table id="table_iqc_zc2_bfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown and Element

</td><td>

Only the scores that match the specified element of this breakdown are shown. Select values for both **Breakdown** and **Element**. Otherwise, only scores that are not associated with any element of the breakdown are shown.

 **Note:** If the widget indicator is on a time series widget, you can specify an elements filter instead of a first-level element. See Step [8](add-indicators-to-widget.md#step_elements-filter).

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

</td></tr><tr><td>

Order

</td><td>

The order in which this indicator appears, if the widget has several secondary indicators. Consider adding extra digits, such as 200 and 300 instead of 2 and 3. This way, if you later add more indicators, you only have to specify the order of the new indicators. You do not have to respecify the order of all secondary indicators.

</td></tr><tr><td>

Chart type

</td><td>

The type of chart for displaying the widget indicator

</td></tr><tr><td>

2nd Y-axis

</td><td>

Add a Y-axis for this indicator.Only one secondary indicator Y-axis is displayed. If a second Y-axis is selected for several secondary indicators, only the axis for the indicator that originally came first in the order is shown.

</td></tr><tr><td>

Color

</td><td>

A single color that applies only to the scores for this indicator.

</td></tr><tr><td>

Label

</td><td>

A custom label for this indicator.

</td></tr></tbody>
</table>7.  To have the widget indicator follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

        Selecting this option removes the ability to set a second breakdown and element on the widget.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to display separate values for the elements of the Assigned to breakdown. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    For more information about breakdown dashboards, see [Using breakdowns on dashboards](../concept/c_SpecialDashboards.md).

8.  Time series widgets only: In the **Elements Filter** tab, you can select an element filter to use instead of selecting a first-level element in the **Element** field.

    See [Element filters](../concept/c_BreakdownElementFilters.md#).

    Use this approach to personalize which breakdowns are shown depending on the viewer. For more information about using element filters to personalize widgets, see [Personalized visuals](../concept/personalized-visuals.md#).

    **Note:** On a dashboard, the names of all the elements that the elements filter passes are appended to the indicator name or label of the widget indicator.

9.  Click **Submit**.


## What to do next

To edit any of these settings later, go to the **Widget Indicators** list and click the information icon for the indicator, not the name.

**Related topics**  


[Related lists](https://www.servicenow.com/docs/access?context=c_RelatedLists&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

[KB0724552: How to Add Secondary Indicators to a Time Series or List Widget](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0724552)

