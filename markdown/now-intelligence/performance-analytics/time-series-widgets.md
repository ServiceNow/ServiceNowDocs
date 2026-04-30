---
title: Time series widgets
description: Time series widgets show changes in an indicator score over time. Different visualizations emphasize the trend in the scores or the scores themselves, and can display one indicator or compare several indicators.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Time series widgets

Time series widgets show changes in an indicator score over time. Different visualizations emphasize the trend in the scores or the scores themselves, and can display one indicator or compare several indicators.

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](../concept/analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

A time series is an ordered sequence of metrics taken continuously over time. Indicator scores are measured over time at uniform intervals, which makes them an appropriate subject for time series widgets. The following business cases are some of the uses of a time series widget:

-   Identifying trends, patterns, and outliers in indicator scores.
-   Identifying turning points, such as whether a change in policy led to a change in indicator scores.
-   Evaluating the relationships between indicators.

When you are selecting a visualization for a time series, consider whether you want to emphasize the trend in the scores or specific changes in the scores. Also consider whether you want to show one indicator or compare several related indicators.

**Note:** Some visualizations of other widget types include a time series. For example, the breakdown widget visualizations Stacked Column and Columns and Total include a time series of the indicator scores.

<table id="table_time-series"><thead><tr><th>

 

</th><th>

Visualization

</th><th>

Description and use case

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Visualizing trends in the scores of an indicator

</td></tr><tr><td>

![Line time series](../../reporting/image/inline-data-vis-96px-line.png)

</td><td>

[Line](../task/create-line-visualization-ts.md)

</td><td>

Shows how one or more values change over time by connecting a series of data points with straight lines. Use a line visualization to emphasize the trend in the scores. Consider line visualizations to be the default choice for displaying a time series. If you are unsure of which visualization to use, use a line.

</td></tr><tr><td>

![Spline time series](../../reporting/image/inline-data-vis-96px-spline.png)

</td><td>

[Spline](../task/create-spline-visualization-ts.md)

</td><td>

Shows how one or more values change over time by connecting a series of data points with a fitted curve through the data points. Spline charts let you take a limited set of known data points and approximate intervening values.

</td></tr><tr><td class="sub-head" colspan="3">

Comparing scores in an indicator

</td></tr><tr><td>

![Column time series](../../reporting/image/inline-data-vis-96px-bar-column.png)

</td><td>

[Column](../task/create-column-visualization-ts.md)

</td><td>

Shows changes between scores over time by displaying them as proportional vertical columns. Use either to visualize score changes in one indicator or to compare indicators. To compare indicators with a column visualization, either add indicators to the widget, or place several column visualization widgets next to each other in a dashboard.

</td></tr><tr><td>

![Step time series](../../reporting/image/inline-data-vis-96px-stepline.png)

</td><td>

[Step](../task/create-step-visualization-ts.md)

</td><td>

Emphasizes changes in indicator scores between discreet points in time. Use to show small incremental changes in scores, especially when a line visualization smudges the data.

</td></tr><tr><td class="sub-head" colspan="3">

Comparing scores or trends between indicators

</td></tr><tr><td>

![](../image/stacked-column-ts.png)

</td><td>

[Stacked Column](../task/create-stacked-col-visualization-ts.md)

</td><td>

Each column is divided into a stack of slices representing different indicators. Use when you want to see the cumulative result of multiple indicators.

</td></tr><tr><td>

![](../image/area-ts-icon.png)

</td><td>

[Area](../task/create-area-visualization-ts.md)

</td><td>

Resembles a line visualization, but the area between the axis and line is emphasized with colors. Use with multiple indicators to highlight the relative contribution that each indicator makes to the whole.

</td></tr><tr><td>

![](../image/relative-compare-icon.png)

</td><td>

[Relative Compare](../task/create-relative-compare-ts.md)

</td><td>

Shows how multiple indicators diverge over time.

</td></tr></tbody>
</table>