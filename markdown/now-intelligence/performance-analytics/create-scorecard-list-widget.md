---
title: Create a scorecard visualization in a list widget
description: To list the metrics of several indicators, use a scorecard visualization in a list widget.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [List widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a scorecard visualization in a list widget

To list the metrics of several indicators, use a scorecard visualization in a list widget.

## Before you begin

Role required: pa\_power\_user or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

Use this visualization to help compare several similar indicators regarding their scores, the trend in their scores, and their compliance with targets.

![Scorecard visualization showing three periods of scores, the target, and the gap between target and the latest score, for new, closed, and open incidents](../image/scorecard-list-widget.png "Scorecard visualization - list widget")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets**.

2.  Click **New**.

3.  In the **Name** field, give the widget a name that reflects the information being displayed.

4.  In the **Type** field, select **List**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

5.  In the **Visualization** field, select **Scorecard**.

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

10. Select the scores and metrics to show in the **Column Settings** tab.

<table id="table_ztf_53r_w1b"><thead><tr><th>

Column setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current score

</td><td>

Show the score from the latest data collection. Selected by default.

</td></tr><tr><td>

Trend

</td><td>

Shows the direction that the indicator is moving. The trend is shown in a mini-chart on the dashboard. Selected by default.

</td></tr><tr><td>

Bullet chart

</td><td>

Show a graphic that shows how close the latest score is to the latest target score. The graphic only appears if the indicator has a defined target.

</td></tr><tr><td>

Multiple scores

</td><td>

Shows the number of scores that are defined in the **Number of periods** field, which appears when **Multiple scores** is selected. If **Current Score** is also selected, the most recent period is labeled **Score**. Otherwise, the most recent period is labeled with the date.

</td></tr><tr><td>

Number of periods

</td><td>

Select the number of additional periods to include in the widget.

</td></tr><tr><td>

Period step

</td><td>

If the **Number of periods** &gt; 1, select the length of each period. The unit is based on the frequency of the first indicator. **Note:** Including indicators with different frequencies, such as daily or weekly, may result in different numbers of periods per indicator. For example, if the first indicator has a daily frequency, and another indicator has a weekly frequency, the daily indicator shows 7 scores for every 1 score of the weekly indicator.

</td></tr><tr><td>

Change

</td><td>

Shows the change in value from the previous score.

</td></tr><tr><td>

Change %

</td><td>

Shows the percentage change from the previous score.

</td></tr><tr><td>

Target

</td><td>

Shows the target for the indicator. A value appears only if the indicator has a defined target. The target and current score are shown graphically in the **Bullet chart**.

</td></tr><tr><td>

Gap

</td><td>

Shows the difference between the current score and the target. For indicators with a Maximize direction, the gap calculation is Score–Target. For indicators with a Minimize direction, the calculation is Target–Score. Thus a positive value is always good, and a negative value is always bad. A value appears only if the indicator has a defined target.

</td></tr><tr><td>

Gap %

</td><td>

Shows the percentage difference between the current and target scores. As with Gap, a positive Gap % is always good, and a negative Gap % is always bad, regardless of the direction of the indicator. A value appears only if the indicator has a defined target.

</td></tr></tbody>
</table>11. Filter which indicators to show in the **List Settings** tab.

    |List setting|Description|
    |------------|-----------|
    |Scorecard options|Select **All** indicators, indicators marked **Key**, or **Favorite** indicators to show only those indicators on the dashboard.|
    |Page size|Select the number of rows to show on the list scorecard.|
    |Filter|Filter the scorecard list for **Best Performing**, **Worst Performing**, **Improved**, **Declined**, or **Deteriorated**. Only indicator scores that match the filter are shown.|

12. Click **Submit** or **Update**.


## What to do next

To view the widget, add it to a dashboard or a portal.

