---
title: Breakdown widgets
description: Breakdown widgets show indicator scores grouped by breakdown elements. Different visualizations can be used to compare the relative proportion of breakdown elements or the trends in these proportions.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Breakdown widgets

Breakdown widgets show indicator scores grouped by breakdown elements. Different visualizations can be used to compare the relative proportion of breakdown elements or the trends in these proportions.

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

When you are selecting a visualization for a breakdown widget, consider whether you want to compare the trends or the relative proportions of the breakdown elements. Also consider whether you want to show one indicator or compare several related indicators, and whether you want to show one or two breakdowns.

| |Visualization|Description|
|---|-------------|-----------|
|Visualizing trends in the scores of an indicator, by elements of a breakdown|
|![Scorecard icon](../image/scorecard-icon.png)|[Scorecard](../task/create-scorecard-widget.md)|Shows the trends for one breakdown for a single indicator.|
|Visualizing the relative proportions of the elements of a breakdown|
|![Data visualization vertical bar type- med](../../reporting/image/inline-data-vis-bar-vertical.png)|[Column](../task/create-column-bkdown-widget.md)|Enables a comparison between the relative proportion of breakdown elements by displaying them as proportional vertical columns. Use when a pie, funnel, or other such visualization is not appropriate.|
|![Data visualization pie type - med](../../reporting/image/inline-data-vis-pie.png)|[Pie](../task/create-pie-widget.md)|Enables a comparison between the relative proportion of breakdown elements by using a circle to represent the whole.|
|![Data visualization donut type - med](../../reporting/image/inline-data-vis-donut.png)|[Donut](../task/create-pie-widget.md)|Enables a comparison between the relative proportion of breakdown elements by using a donut shape to represent the whole.|
|![Data visualization semi-donut type - med](../../reporting/image/inline-data-vis-semi-donut.png)|[Semi-donut](../task/create-pie-widget.md)|Enables a comparison between the relative proportion of breakdown elements by using a semi-donut shape to represent the whole. A semi-donut chart uses a donut sliced in half to represent the whole.|
|![Funnel icon](../../../administer/process-mining/image/funnel-icon.png)|[Funnel](../task/create-pyramid-funnel-widget.md)|Enables a comparison between the relative proportion of breakdown elements by displaying values as progressively decreasing proportions. The size of each section reflects a percentage of the total of all values.|
|![Pyramid icon](../image/pyramid-icon.png)|[Pyramid](../task/create-pyramid-funnel-widget.md)|Enables a comparison between the relative proportion of breakdown elements by displaying values as progressively increasing proportions. The size of each section reflects a percentage of the total of all values.|
|Visualizing both the trend in scores and the relative proportions of elements of a breakdown|
|![Stacked column breakdown widget icon](../image/stacked-column-bkdown-icon.png)|[Stacked Column](../task/create-stacked-column-bkdown-widget.md)|Combines time series and breakdown widget functions. The X-axis is a time line and the visualization shows the development of indicator scores over time. Also, each column is divided into a stack of slices according to the elements of a breakdown. Thus the visualization shows the relative proportion of breakdown elements over time.|
|![Column widget icon](../image/columns-total-icon.png)|[Column and total](../task/create-column-total-bkdown-widget.md)|Shows both the relative proportion of breakdown elements and the trend in the indicator score. Shows a separate column for each breakdown value and a line representing the total for all values, over time.|
|![Line visualization in breakdown widget](../image/line-bkdown-icon.png)|[Line](../task/create-line-bkdown-widget.md)|Shows changes over time in the relative proportion of breakdown elements for an indicator by connecting a series of data points with straight lines.|
|![Relative compare icon](../image/relative-compare-icon.png)|[Relative Compare](../task/create-relative-compare-bkdn.md)|Shows how multiple breakdowns diverge over time.|
|Other visualizations|
|![Pareto visualization icon](../image/pareto-icon.png)|[Pareto](../task/create-pareto-bkdown-widget.md)|Combines column and line visualizations to identify the most important factors in a large set of factors.|
|![Scorecard icon](../image/pivot-scorecard-icon.png)|[Pivot scorecard](../task/create-pivot-scorecard-breakdown.md)|Enables you to compare the breakdown elements for one breakdown applied to several indicators. The Y-axis can be the indicators or the breakdown elements.|
|![Treemap icon](../image/treemap-icon.png)|[Treemap](../task/create-treemap-breakdown.md)|Shows a treelike display of nested rectangles with a color gradient to signify positive to negative scores or trends in scores.|

