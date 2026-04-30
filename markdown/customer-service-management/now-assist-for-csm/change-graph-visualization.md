---
title: Change graph visualization
description: Change a graph visualization to a different type within the same graph group, such as converting a horizontal bar chart to a vertical bar chart or an area chart to a line chart.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 1
keywords: [Generative AI, Generative AI for Customer Service Management, Generative AI for customer service agents]
breadcrumb: [Trending topics dashboard, Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Change graph visualization

Change a graph visualization to a different type within the same graph group, such as converting a horizontal bar chart to a vertical bar chart or an area chart to a line chart.

## Before you begin

Role required: admin or maint

## About this task

This procedure allows you to change a graph to a different visualization type within the same group. The following are similar groups of graphs:

-   Scores: Single score, Dial, Gauge
-   Time series: Area, Column, Line, Scatter, Spline, Step
-   Bars: Horizontal bar, Vertical bar, Pareto
-   Pies and donuts: Donut, Pie, Semi Donut
-   Multidimensional charts: Pivot table, Heatmap, Bubble

**Tip:** Changing between graphs in the same group is very easy. For example, an area chart can be converted to any other time series chart such as spline, column, or line.

## Procedure

1.  Navigate to **All** &gt; **UI Builder**

2.  Under **Components** tab select the corresponding component that contains the graph you want to change.

    For example, open **Topic Over Time Visualization**.

    If needed, create a clone of the component before making changes.

3.  Select the graph on the left panel that you want to change.

4.  Locate the **Data visualization type** field.

5.  Change the graph type to a different visualization within the same graph group.

    **Important:** Ensure the new graph type is within the same group as the original graph type. Converting across different graph groups is very difficult and may require significant programming changes.

6.  Select **Save**.

    The graph visualization type is updated and displays data in the new format.


**Related topics**  


[Configure trending topics dashboard](configure-trending-topics-dashboard.md)

[Add a new filter](add-a-new-filter.md)

[Change an insight to use a different field for trending topics](change-insight-to-use-a-different-field.md)

