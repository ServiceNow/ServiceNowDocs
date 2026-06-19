---
title: Breakdown widgets
description: Breakdown widgets show indicator scores grouped by breakdown elements. Different visualizations can be used to compare the relative proportion of breakdown elements or the trends in these proportions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/breakdown-widgets.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Breakdown widgets

Breakdown widgets show indicator scores grouped by breakdown elements. Different visualizations can be used to compare the relative proportion of breakdown elements or the trends in these proportions.

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/interactive-filters-workspace.md).

This feature is deprecated, meaning it is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

When you are selecting a visualization for a breakdown widget, consider whether you want to compare the trends or the relative proportions of the breakdown elements. Also consider whether you want to show one indicator or compare several related indicators, and whether you want to show one or two breakdowns.

| |Visualization|Description|
|---|-------------|-----------|
|Visualizing trends in the scores of an indicator, by elements of a breakdown|
|\[Omitted image "scorecard-icon.png"\] Alt text: Scorecard icon|[Scorecard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-scorecard-widget.md)|Shows the trends for one breakdown for a single indicator.|
|Visualizing the relative proportions of the elements of a breakdown|
|\[Omitted image "inline-data-vis-bar-vertical.png"\] Alt text: Data visualization vertical bar type- med|[Column](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-column-bkdown-widget.md)|Enables a comparison between the relative proportion of breakdown elements by displaying them as proportional vertical columns. Use when a pie, funnel, or other such visualization is not appropriate.|
|\[Omitted image "inline-data-vis-pie.png"\] Alt text: Data visualization pie type - med|[Pie](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-pie-widget.md)|Enables a comparison between the relative proportion of breakdown elements by using a circle to represent the whole.|
|\[Omitted image "inline-data-vis-donut.png"\] Alt text: Data visualization donut type - med|[Donut](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-pie-widget.md)|Enables a comparison between the relative proportion of breakdown elements by using a donut shape to represent the whole.|
|\[Omitted image "inline-data-vis-semi-donut.png"\] Alt text: Data visualization semi-donut type - med|[Semi-donut](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-pie-widget.md)|Enables a comparison between the relative proportion of breakdown elements by using a semi-donut shape to represent the whole. A semi-donut chart uses a donut sliced in half to represent the whole.|
|\[Omitted image "funnel-icon.png"\] Alt text: Funnel icon|[Funnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-pyramid-funnel-widget.md)|Enables a comparison between the relative proportion of breakdown elements by displaying values as progressively decreasing proportions. The size of each section reflects a percentage of the total of all values.|
|\[Omitted image "pyramid-icon.png"\] Alt text: Pyramid icon|[Pyramid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-pyramid-funnel-widget.md)|Enables a comparison between the relative proportion of breakdown elements by displaying values as progressively increasing proportions. The size of each section reflects a percentage of the total of all values.|
|Visualizing both the trend in scores and the relative proportions of elements of a breakdown|
|\[Omitted image "stacked-column-bkdown-icon.png"\] Alt text: Stacked column breakdown widget icon|[Stacked Column](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-stacked-column-bkdown-widget.md)|Combines time series and breakdown widget functions. The X-axis is a time line and the visualization shows the development of indicator scores over time. Also, each column is divided into a stack of slices according to the elements of a breakdown. Thus the visualization shows the relative proportion of breakdown elements over time.|
|\[Omitted image "columns-total-icon.png"\] Alt text: Column widget icon|[Column and total](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-column-total-bkdown-widget.md)|Shows both the relative proportion of breakdown elements and the trend in the indicator score. Shows a separate column for each breakdown value and a line representing the total for all values, over time.|
|\[Omitted image "line-bkdown-icon.png"\] Alt text: Line visualization in breakdown widget|[Line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-line-bkdown-widget.md)|Shows changes over time in the relative proportion of breakdown elements for an indicator by connecting a series of data points with straight lines.|
|\[Omitted image "relative-compare-icon.png"\] Alt text: Relative compare icon|[Relative Compare](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-relative-compare-bkdn.md)|Shows how multiple breakdowns diverge over time.|
|Other visualizations|
|\[Omitted image "pareto-icon.png"\] Alt text: Pareto visualization icon|[Pareto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-pareto-bkdown-widget.md)|Combines column and line visualizations to identify the most important factors in a large set of factors.|
|\[Omitted image "pivot-scorecard-icon.png"\] Alt text: Scorecard icon|[Pivot scorecard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-pivot-scorecard-breakdown.md)|Enables you to compare the breakdown elements for one breakdown applied to several indicators. The Y-axis can be the indicators or the breakdown elements.|
|\[Omitted image "treemap-icon.png"\] Alt text: Treemap icon|[Treemap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-treemap-breakdown.md)|Shows a treelike display of nested rectangles with a color gradient to signify positive to negative scores or trends in scores.|

