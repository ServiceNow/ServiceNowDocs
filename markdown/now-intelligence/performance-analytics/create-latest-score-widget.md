---
title: Create a latest score visualization for a score widget
description: To see the change between the latest score and a previous score, use a latest score visualization in a score widget. You can also show a trend line of scores.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Score widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a latest score visualization for a score widget

To see the change between the latest score and a previous score, use a latest score visualization in a score widget. You can also show a trend line of scores.

## Before you begin

Role required: pa\_admin or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is deprecated, meaning it is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

A latest score visualization shows the latest score and both the absolute and percentage change between this score and a previous score. This visualization is similar to a **Chart** view in an Analytics Hub. You can choose how many scores back to compare to the latest score. You can also display a trend line of absolute or percentage changes in scores.

**Note:** This data visualization is supported on the mobile platform. For more information, see [Displaying KPI Details for the mobile dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-reporting-pa-widgets.md) and [Mobile dashboard preview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-dashboard-preview.md).

![Latest score visualization of the percentage of incidents resolved without reassignment](../image/latest-score-widget.png "Latest score visualization")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets** and click **New**.

2.  In the **Name** and **Subtitle** fields, give the widget a name and subtitle that reflect the information being displayed.

3.  In the **Type** field, select **Score**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

4.  In the **Visualization** field, select **Latest score**.

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

8.  Select a template.

    |Template name|Description|
    |-------------|-----------|
    |**Template 1**|Line shows absolute change in score.|
    |**Template 2**|Line shows percentage change in score.|
    |**Template 3**|Line is not displayed.|

    [Formula indicators](t_CreateAFormulaIndicator.md) that return a percentage value use Template 2 by default. Other indicators use Template 1 by default.

9.  In the **Latest score settings** tab, select which previous score to compare against the latest score in the **Compare score with** field:

<table id="table_ft5_nhr_w2b"><tbody><tr><td>

Previous score

</td><td>

The score from the previous data collection. This setting is the default.

</td></tr><tr><td>

Periods back

</td><td>

Specify the number of data collection periods back from which you want the score to compare against the latest score.

</td></tr></tbody>
</table>10. In the **Element Settings** tab, you can select an element filter instead of selecting a specific element in the **Element** field.

    Use this approach to personalize which breakdowns are shown depending on the viewer. For more information about using element filters to personalize widgets, see [Personalized visuals](../concept/personalized-visuals.md#).

11. Click **Submit**.


## What to do next

To view the widget, add it to a dashboard or a portal.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[View scores and statistics](../concept/scorecard-overview-tab.md#)

