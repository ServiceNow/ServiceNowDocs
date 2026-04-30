---
title: Create a pivot scorecard visualization for a breakdown widget
description: To compare the relative proportions of breakdown elements between a number of indicators, use a pivot scorecard visualization in a breakdown widget.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Breakdown widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a pivot scorecard visualization for a breakdown widget

To compare the relative proportions of breakdown elements between a number of indicators, use a pivot scorecard visualization in a breakdown widget.

## Before you begin

Role required: pa\_power\_user or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

If you want to see the same breakdown applied to more than one indicator in the same widget, use a pivot scorecard. You can pivot the scorecard so that the axes for breakdown elements and for indicators are reversed.

![Pivot scorecard visualization of several open incident indicators by priority](../image/pivot-scorecard-bkdown.png "Pivot scorecard - breakdown")

![Pivot scorecard visualization of several open incident indicators by priority, with the elements of the priority breakdown on the Y-axis](../image/pivot-scorecard-bkdown-on-y.png "Pivot scorecard with the breakdown on the Y-axis")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets** and click **New**.

2.  In the **Name** field, give the widget a name that reflects the information being displayed.

3.  In the **Type** field, select **Breakdown**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

4.  In the **Visualization** field, select **Pivot Scorecard**.

5.  In the **Pivot breakdown** field, select the breakdown whose elements you want to see across several indicators.

6.  Click **Save**.

    The **Indicators** related list appears at the bottom of the form.

7.  In the **Indicators** related list, click **New**.

8.  In the menu that appears, select the indicators that you want to compare breakdown elements between.

9.  Click **Update**.


## What to do next

-   To view the widget, add it to a dashboard or a portal.
-   Once the widget is in a dashboard, edit the widget and try the **Breakdown on Y-axis** display setting.

**Related topics**  


[Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md)

[Performance Analytics widgets on Service Portal](../concept/service-portal-pa-widget.md#)

[Grouping by breakdown and filtering by breakdown](../concept/grouping-filtering-breakdown.md)

