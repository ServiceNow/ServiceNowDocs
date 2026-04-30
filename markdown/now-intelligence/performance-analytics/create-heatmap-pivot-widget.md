---
title: Create a heatmap visualization in a pivot widget
description: To group the scores of an indicator by two breakdowns, use a heatmap visualization in a pivot widget.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a heatmap visualization in a pivot widget

To group the scores of an indicator by two breakdowns, use a heatmap visualization in a pivot widget.

## Before you begin

Role required: pa\_power\_user or admin

## About this task

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

If you want to apply two breakdowns to an indicator, create a pivot widget with the breakdowns as the two axes of the pivot table. Heatmaps, which use a color gradient to highlight when both scores are high, are the only visualization available for pivot widgets.

**Note:**

-   Pivot widgets do not support the **Follow Element** function. Dashboard breakdowns cannot apply to these widgets.
-   Heatmaps cannot display more than 1000 cells. If the total number of elements of the two breakdowns is above 1000, the heatmap does not appear.

![Heatmap visualization of open incidents by priority and category](../image/heatmap-pivot-widget.png "Heatmap visualization - pivot widget")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets**.

2.  Click **New**.

3.  In the **Name** field, give the widget a name that reflects the information being displayed.

4.  In the **Type** field, select **Pivot**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

5.  In the **Visualization** field, select **Heatmap**.

6.  In the **Indicator** field, select the indicator which you want to break down.

7.  In the **Breakdown** field, select the breakdown to be the X-axis.

8.  In the **2nd Breakdown** field, select the breakdown to be the Y-axis.

9.  In the **Display Settings**, set the color scheme and whether to display data labels and the legend.

10. Click **Submit**.


## What to do next

To view the widget, add it to a dashboard or a portal.

