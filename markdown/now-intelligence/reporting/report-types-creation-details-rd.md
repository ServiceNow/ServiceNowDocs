---
title: Report types
description: Learn about the different types of reports that you can create, and when and how to create them.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2025-12-02"
reading_time_minutes: 9
breadcrumb: [Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report types

Learn about the different types of reports that you can create, and when and how to create them.

Watch this four-minute video to learn how to create and configure a report visualization.

How to create, style, and share reports in Core UI 

You can generate the following types of reports, organized by category:

-   [Bar reports](report-types-creation-details-rd.md#table_xwp_vqq_5x) enable you to compare scores across data dimensions.
-   [Pie and Donut reports](report-types-creation-details-rd.md#table_lky_gfn_nhb) visualize the relationship between the parts and the whole of a data set using a single round shape.
-   [Time Series reports](report-types-creation-details-rd.md#table_e1q_xqq_5x) visualize data over time. In addition to data from within your instances and imported data sources, you can also use MetricBase data in time series reports. For more information, see [MetricBase application](https://www.servicenow.com/docs/access?context=metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   [Multidimensional reports](report-types-creation-details-rd.md#table_i11_yqq_5x) visualize data across dimensions in a single table or graph.
-   [Scores](report-types-creation-details-rd.md#table_sth_yqq_5x) visualize single data points either across ranges or as a single value.
-   [Statistical reports](report-types-creation-details-rd.md#table_g3p_yqq_5x) visualize data with statistical values such as medians and means.
-   [Other reports](report-types-creation-details-rd.md#table_ac1_zqq_5x) include calendars, maps, and lists.

You can also use Natural Language Query \(NLQ\) inside Report Designer to generate a report. Simply write a question into the NLQ field, and the Report Designer generates a report of an appropriate type.

<table id="table_xwp_vqq_5x"><thead><tr><th>

 

</th><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Data visualization vertical bar type - icon](../image/inline-data-vis-bar-vertical.png)![Data visualization horizontal bar type - icon](../image/inline-data-vis-bar-horizontal.png)

</td><td>

[Vertical and horizontal bar reports](../concept/c_CreateBarCharts.md#)

</td><td>

Shows vertical or horizontal bars with lengths proportional to the values that they represent.

</td></tr><tr><td>

![Data visualization pareto type - icon](../image/inline-data-vis-pareto.png)

</td><td>

[Pareto reports](../concept/c_CreateParetoCharts.md#)

</td><td>

Combines bar and line reports to identify the most important factors in a large set of factors.

</td></tr><tr><td>

![Data visualization histogram type - icon](../image/inline-data-vis-histogram.png)

</td><td>

[Histogram reports](../concept/c_CreatingHistograms.md#)

</td><td>

Provides visual interpretation of numerical data by indicating the number of data points that lie within a range of values.

</td></tr></tbody>
</table>| |Report|Description|
|---|------|-----------|
|![Data visualization pie type - icon](../image/inline-data-vis-pie.png)|[Pie charts](../concept/c_CreatePieCharts.md#)|Shows how individual pieces of data relate to the whole using a circle to represent the whole.|
|![Data visualization donut type - icon](../image/inline-data-vis-donut.png)|[Donut reports](../concept/c_CreateDonutCharts.md#)|Shows how individual pieces of data relate to the whole using a donut shape to represent the whole.|
|![Data visualization semi-donut type - icon](../image/inline-data-vis-semi-donut.png)|[Semi-donut reports](../concept/c_CreateDonutCharts.md#)|Shows how individual pieces of data relate to the whole using a semi-donut shape to represent the whole. A semi-donut report uses a donut sliced in half to represent the whole.|

| |Report|Description|
|---|------|-----------|
|![Data visualization column type - icon](../image/inline-data-vis-bar-column.png)|[Column reports](../concept/c_CreateColumnCharts.md#)|Shows how one or more values change over time by displaying them as proportional vertical columns.|
|![Data visualization line type - icon](../image/inline-data-vis-line.png)|[Line reports](../concept/c_CreateLineCharts.md#)|Shows how one or more values change over time by connecting a series of data points with straight lines.|
|![Data visualization step line type - icon](../image/inline-data-vis-stepline.png)|[Step line reports](../concept/step-reports.md#)|Shows how one or more values change over time by connecting a series of data points with horizontal and vertical lines.|
|![Data visualization area type - icon](../image/inline-data-vis-area.png)|[Area reports](../concept/c_CreateAreaAndSplineCharts.md#)|Resembles a line chart, but the area between the axis and line is commonly emphasized with colors.|
|![Data visualization spline type - icon](../image/inline-data-vis-spline.png)|[Spline reports](../concept/c_CreateAreaAndSplineCharts.md#)|Shows how one or more values change over time by connecting a series of data points with a fitted curve through the data points. Spline reports let you take a limited set of known data points and approximate intervening values.|

| |Report|Description|
|---|------|-----------|
|![Data visualization pivot table type - icon](../image/inline-data-vis-pivot-table.png)|[Multilevel pivot tables](../concept/c_MultilevelPivotCharts.md#)|Displays aggregate data broken down by multiple metrics in a single chart.|
|![Data visualization heatmap type - icon](../image/inline-data-vis-heatmap.png)|[Heatmap reports](../concept/c_HeatmapCharts.md#)|Displays aggregate data in a matrix using colors to represent different values.|
|![Data visualization bubble type - icon](../image/inline-data-vis-bubble.png)|[Bubble reports](../concept/c_BubbleCharts.md#)|Displays multiple metrics on a single chart.|

| |Report|Description|
|---|------|-----------|
|![Data visualization speedometer type - icon](../image/inline-data-vis-speedometer.png)|[Speedometer reports](../concept/c_CreateDialsAndSpeedometers.md#)|Shows an overview of the count of an indicator at the current moment in the form of a round meter.|
|![Data visualization dial type](../image/inline-data-vis-dial.png)|[Dial reports](../concept/c_CreateDialsAndSpeedometers.md#)|Shows an overview of the count of an indicator that you want to measure in a half circle. The part in which scores are shown is filled with a color.|
|![Data visualization single score type - icon](../image/inline-data-vis-single-score.png)|[Single score report](../concept/c_SingleScoreCharts.md#)|Displays a single aggregate value that is important to your business.|

| |Report|Description|
|---|------|-----------|
|![Data visualization - control type - icon](../image/inline-data-vis-control.png)|[Control reports](../concept/c_CreatingControlCharts.md#)|Displays data as a series of connected points to determine whether a business process is in a state of statistical control and to identify outliers. \(Found in the Other reports section.\)|
|![Data visualization trend type - icon](../image/inline-data-vis-trend.png)|[Trend reports](../concept/c_CreateTrendCharts.md#)|Shows how the value of one or more items changes over time. Values along the horizontal axis of the trend report represent the time measurement. Values on the vertical axis represent the changes to the items being monitored. The trend line or curve reveals a general pattern of change. \(Found in the Other reports section.\)|
|![Data visualization vertical box type - icon](../image/inline-data-vis-box.png)|[Box reports](../concept/c_CreatingBoxCharts.md#)|Shows the distribution of values in a data set highlighting statistical averages. \(Found in the Other reports section.\)|
|![Data visualization vertical box type - icon](../image/inline-data-vis-box.png)|[Trendbox reports](../concept/c_CreatingTrendboxCharts.md#)|Shows the distribution of values in a data set highlighting statistical averages for a specified periodof. \(Found in the Other reports section.\)|

| |Report|Description|
|---|------|-----------|
|![Data visualization funnel type - icon](../image/inline-data-vis-funnel.png)|[Funnel reports](../concept/c_CreateFunnelAndPyramidCharts.md#)|Displays values as progressively decreasing proportions. The size each section reflects a percentage of the total of all values.|
|![Data visualization scorecard type - icon](../image/inline-data-vis-scorecard.png)|[List reports](../concept/list-reports.md)|Displays data in the form of an expandable list, similar to a standard ServiceNow [list component](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/shared-components/now-record-list-connected/overview).|
|![Data visualization calendar type - icon](../image/inline-data-vis-calendar-days.png)|[Calendar reports](../concept/c_CalendarReport.md#)|Displays data-driven events in a calendar format.|
|![Data visualization geomap type - icon](../image/inline-data-vis-geomap.png)|[Map reports](../concept/c_MapReport.md#)|Displays data on a geographical map image.|
|![Data visualization pivot table type - large](../image/inline-data-vis-96px-pivot-table.png)|[Pivot tables](../concept/c_PivotTables.md#)|Aggregates data from a table to display the source of summarized data. This functionality is expanded in [multilevel pivot reports](../concept/c_MultilevelPivotCharts.md#).|
|![Data visualization pyramid type - large](../image/inline-data-vis-96px-pyramid.png)|[Pyramid reports](../concept/c_CreateFunnelAndPyramidCharts.md#)|Visualizes a variation on a bar report using pyramid sections instead of rectangles. \(Found in the Other reports section.\)|

## Choosing a report type

Choose a report type based on the story that you want data to tell.

![Report type uses](../image/data-vis-diagram.png)

