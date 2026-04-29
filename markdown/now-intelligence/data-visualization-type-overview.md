---
title: Overview of data visualization types
description: When you create a data visualization, you select the type of visualization to display. Each visualization type is suited to show different data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Overview of data visualization types

When you create a data visualization, you select the type of visualization to display. Each visualization type is suited to show different data.

## Score visualizations

This type of data visualization shows a single value or score as a number or percentage. Scores are often used to show how a particular value or metric compares to a target or benchmark. They can be useful for tracking progress or identifying areas for improvement, for example showing a company's or division's overall performance.

<table id="table_sth_yqq_5x"><thead><tr><th>

Visualization

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Single score visualization](../../reporting/task/create-dv-sing-sc-ac.md) ![](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Single-score visualizations display a single aggregate value that is important to your business.[Single score data visualization example](../task/dv-example-single-score.md)

</td></tr><tr><td>

[Dial visualization](../../reporting/task/create-dv-dial-ac.md) ![](../../reporting/image/inline-data-vis-dial.png)

</td><td>

Dial visualizations show where a single value lies across a range from minimum to maximum expected values. Visually, a "needle" points to the value, and the dial is colored in for values up to the needle.[Dial visualization example](../task/dv-example-dial.md)

</td></tr><tr><td>

[Gauge visualization](../../reporting/task/create-dv-gauge-ac.md) ![](../../reporting/image/inline-data-vis-gauge.png)

</td><td>

Like dials, gauges show where a single value lies across a range from minimum to maximum expected values. In addition to dial functionality, you can set colored data ranges to help users understand what the value represents.[Gauge visualization example](../task/dv-example-gauge.md)

</td></tr></tbody>
</table>## Time series visualizations

Time Series visualizations show data over time. All time series visualization types share configuration options. They differ in use case, depending on whether you want to emphasize data trends or the differences between individual data points. For more information about these use cases, see [Create time series data visualizations](../../reporting/task/create-dv-time-series-ac.md).

**Note:** In addition to data from within your instances and imported data sources, you can also use MetricBase data in time series visualizations. For more information, see [MetricBase application](https://www.servicenow.com/docs/access?context=metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

<table id="table_time-series"><thead><tr><th>

Visualization

</th><th>

Description and use case

</th></tr><tr><th class="sub-head" colspan="2">

Visualizing trends in a data source

</th></tr></thead><tbody><tr><td>

Line![line visualization](../../reporting/image/inline-data-vis-line.png)

</td><td>

Shows how one or more values change over time by connecting a series of data points with straight lines. Use a line visualization to emphasize the trend in the data. Consider line visualizations to be the default choice for showing a time series. If you’re unsure of which visualization to use, use a line.

</td></tr><tr><td>

Spline![spline visualization](../../reporting/image/inline-data-vis-spline.png)

</td><td>

Shows how one or more values change over time by connecting a series of data points with a fitted curve. The curve emphasizes the trend over individual data points. Spline visualizations let you take a limited set of known data points and approximate intervening values.

</td></tr><tr><td>

Scatter![scatter visualization - med](../../reporting/image/inline-data-vis-trend.png)

</td><td>

Shows unconnected points for values in the Y-axis against time in the X-axis. Usually the trend line is also shown. Use with a spread of data that can’t be usefully connected with a line.

</td></tr><tr><td class="sub-head" colspan="2">

Comparing scores in a data source

</td></tr><tr><td>

Column![column visualization](../../reporting/image/inline-data-vis-bar-column.png)

</td><td>

Shows changes in data over time by showing values as proportional vertical columns. Use either to visualize changes in one data source or to compare data sources. To compare data sources with a column visualization, either add data sources to the visualization, or place several column visualizations next to each other in a dashboard.

</td></tr><tr><td>

Step![](../../reporting/image/inline-data-vis-stepline.png)

</td><td>

Emphasizes changes in a data source between discreet points in time. Use to show small incremental changes, especially when a line visualization smudges the data.

</td></tr><tr><td class="sub-head" colspan="2">

Comparing scores or trends between data sources

</td></tr><tr><td>

Area![](../../reporting/image/inline-data-vis-area.png)

</td><td>

Resembles a line visualization, but the area between the axis and line is emphasized with colors. Use with multiple data sources to highlight the relative contribution that each data source makes to the whole.

</td></tr></tbody>
</table>## Bar visualizations

Bar visualizations enable you to compare scores across data dimensions. Horizontal and vertical bar visualization types are available. They share all configuration options. In general, use horizontal bars for nominal or categorical data. Use vertical bars for ordinal or sequential data. Use different colors or patterns to distinguish different groups or categories. For more information, see [Create a horizontal or vertical bar data visualization](../../reporting/task/create-dv-bar-ac.md).

<table id="table_js4_h4f_s5b"><thead><tr><th>

Visualization

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Horizontal bar visualization](../../reporting/task/create-dv-bar-ac.md) ![](../../reporting/image/inline-data-vis-bar-horizontal.png)

</td><td rowspan="3">

Bar visualizations show categories labeled on one axis and values on the other. Use vertical bars to compare ordinal data, especially when there aren’t too many categories, such as sales numbers grouped into buckets. Use horizontal bar charts with nominal data, such as incident severity or assignment group.-   [Horizontal bar visualization example](../task/dv-example-h-bar.md)
-   [Vertical bar visualization example](../task/dv-example-v-bar.md)

Pareto bar visualizations help you identify the most important dimension in a large set of dimensions. Columns show data in descending order. A line shows cumulative percentage. Pareto visualizations contain both bar and line graphs. The bars display the data in descending order from left to right, and the line graph shows the cumulative totals from each category in the same order. The left Y axis is the record count, and the right Y axis is the cumulative percentage of the total number of records evaluated.

</td></tr><tr><td>

[Vertical bar visualization](../../reporting/task/create-dv-bar-ac.md) ![Data visualization vertical bar type- med](../../reporting/image/inline-data-vis-bar-vertical.png)

</td></tr><tr><td>

[Pareto bar visualization](../../reporting/task/create-dv-pareto-vd.md)![Data visualization pareto bar type](../../reporting/image/inline-data-vis-pareto.png)

</td></tr></tbody>
</table>## Pie and Donut visualizations

Pie and donut visualizations show the relationship between parts and the whole of a data set. The segments of these visualizations should total to 100%. For more information, see [Create a pie or donut data visualization](../../reporting/task/create-dv-donut-ac.md).

<table id="table_vks_frf_s5b"><thead><tr><th>

Visualization

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Pie visualizations](../../reporting/task/create-dv-donut-ac.md) ![](../../reporting/image/inline-data-vis-pie.png)

</td><td rowspan="3">

Pie visualizations are best when comparing 5–7 segments that total 100%, when no two segments have a value within 10% of each other.

 Donut visualizations are best for comparing no more than five segments that total 100%, when no two segments have a value within 10% of each other. The center of the donut can be used to show additional information.

 Semi-donut visualizations are best for comparing no more than four segments that total 100%, when no two segments have a value within 10% of each other.

 -   [Pie visualization example](../task/dv-example-pie.md)
-   [Donut visualization example](../task/dv-example-donut.md)

</td></tr><tr><td>

[Donut visualizations](../../reporting/task/create-dv-donut-ac.md) ![](../../reporting/image/inline-data-vis-donut.png)

</td></tr><tr><td>

[Semi-donut visualizations](../../reporting/task/create-dv-donut-ac.md) ![](../../reporting/image/inline-data-vis-semi-donut.png)

</td></tr></tbody>
</table>## Multidimensional charts

Multidimensional visualizations enable you to show multiple variables in a single chart, and it can be useful for showing the relationships between different variables. They are useful when you have a lot of data, and you want to find patterns or trends that might not be immediately obvious. They're also good to use when you want to show the relationship between three or more variables.

<table id="table_uyz_dtf_s5b"><thead><tr><th>

Visualization

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Pivot table visualization](../../reporting/task/create-dv-pivot-ac.md) ![Data visualization pivot table type - med](../../reporting/image/inline-data-vis-pivot-table.png)

</td><td>

Pivot tables allow for several kinds of aggregation between its fields. You can also filter the data. The columns represent one field or [breakdown](../../performance-analytics/concept/performance-analytics-glossary.md#), while a hierarchy of rows represents multiple other fields or breakdowns.[Pivot visualization example](../task/dv-example-pivot.md)

</td></tr><tr><td>

[Heatmap visualization](../../reporting/task/create-dv-heatmap-ac.md) ![Data visualization heatmap type - med](../../reporting/image/inline-data-vis-heatmap.png)

</td><td>

Heatmaps show the relationship between two table fields or indicator breakdowns. The changes in color as you move along the axes reveal patterns in the value of one or both fields/breakdowns.[Heatmap visualization example](../task/dv-example-heatmap.md)

</td></tr><tr><td>

[Bubble chart visualization](../../reporting/task/create-dv-bubble-ac.md) ![Data visualization bubble chart - med](../../reporting/image/inline-data-vis-bubble.png)

</td><td>

Bubble charts are circles of different sizes along an x-y axis. The x and y axes represent different numeric fields, such as values or amounts. Use the relative size and position of the circles to compare fields and see their relationships. You can also group the data by a third field, which can be qualitative. The third field is differentiated by color. Use bubble charts to answer binary questions, such as whether two fields have a relationship, and to highlight patterns.[Bubble data visualization example](../task/dv-example-bubble.md)

</td></tr></tbody>
</table>## Other visualizations

Data visualizations can also show calendars, simple lists, indicator scorecards, and location.

<table id="table_bcx_f2r_g5b"><thead><tr><th>

Visualization

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Calendar report visualization](../../reporting/task/create-dv-calendar-ac.md) ![Data visualization calendar type - med](../../reporting/image/inline-data-vis-calendar-days.png)

</td><td>

Displays data-driven events in a calendar format.

</td></tr><tr><td>

[Indicator scorecard](../../reporting/task/create-dv-indicator-scorecard.md#) ![Analytics center scorecard report-med](../../reporting/image/inline-data-vis-scorecard.png)

</td><td>

The Indicator scorecard component enables you to visualize and compare data between multiple Performance Analytics indicators.[Create an Indicator Scorecard](../../reporting/task/create-dv-indicator-scorecard.md)

</td></tr><tr><td>

[List](../../reporting/task/create-dv-analytics-list.md)![Data visualization list type - med](../../reporting/image/inline-data-vis-list.png)

</td><td>

Shows a list of table records.

</td></tr><tr><td>

[Box plot](../../reporting/task/create-dv-box-plot.md)![](../../reporting/image/inline-data-vis-box.png)

</td><td>

Use a box plot to show the median and lower and upper quartiles of numeric data along with outliers. You can also compare the distribution of different groups of this data.

</td></tr><tr><td>

[Geomap](../../reporting/task/create-dv-geomap-ac.md)![Geomap data visualization](../../reporting/image/inline-data-vis-geomap.png)

</td><td>

Displays data by country, state, or city. Users can use table data that contains location information to visualize in the chart.

</td></tr></tbody>
</table>**Parent Topic:**[Creating data visualizations](../../reporting/concept/creating-data-visualizations.md)

