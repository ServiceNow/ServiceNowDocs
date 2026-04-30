---
title: Creating data visualizations
description: See how to create data visualizations using different data sources.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2026-01-06"
reading_time_minutes: 5
keywords: [Create visualization, Create data visualization]
breadcrumb: [Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Creating data visualizations

See how to create data visualizations using different data sources.

How to create a data visualization in the Visualization Designer. 

**Note:** In the Yokohamarelease, visualizations are based on Highcharts version 10.3.3.

Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## Creating data visualizations in a dashboard editor

To create a data visualization from a dashboard, select **Add new element** and then choose **New visualization**. You can then configure the visualization as described in the topic for the selected visualization type.![Open dashboard in edit mode with the Add new element and New visualization buttons highlighted](../image/new-dv-from-dashboard.png)

## Creating data visualizations in the Visualization Designer

To create data visualizations in the Visualization Designer, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**. You can then configure the visualization as described in the topic for the selected visualization type.

![Data visualizations selected in filter navigator and New button highlighted](../image/new-dv.png)

## Instructions for creating data visualizations by type

-   **[Overview of data visualization types](../../par-for-workspace/concept/data-visualization-type-overview.md)**  
When you create a data visualization, you select the type of chart to display. Each visualization type is suited to show different data.
-   **[Create a single score data visualization in the Visualization Designer or on a dashboard](../task/create-dv-sing-sc-ac.md)**  
Use a single score to show a value as a number or percentage. Visualize how the value compares to a target or benchmark, to track progress, or to identify areas for improvement.
-   **[Create a box plot data visualization](../task/create-dv-box-plot.md)**  
Use a box plot to show the median and lower and upper quartiles of numeric data along with outliers. You can also compare the distribution of different groups of this data.
-   **[Create a bubble visualization in the Visualization Designer](../task/create-dv-bubble-ac.md)**  
Use a bubble visualization to show multiple separate metrics on a single chart. Use bubble charts to answer binary questions, such as whether two fields have a relationship, and to highlight patterns.
-   **[Create a dial visualization in the Visualization Designer](../task/create-dv-dial-ac.md)**  
Use a dial visualization to show where a value lies between expected minimum and maximum values. Use the dial visualization to show how a value compares to a target or benchmark, track progress, or to identify areas for improvement.
-   **[Create a gauge visualization in the Visualization Designer](../task/create-dv-gauge-ac.md)**  
A gauge visualization shows where a value lies between expected minimum and maximum values. Use the gauge visualization to follow progress with color-coded value ranges.
-   **[Create a geomap visualization in the Visualization Designer](../task/create-dv-geomap-ac.md)**  
A geomap visualization shows the geographical distribution of data for a world, country, region, or province/state. Use Geomaps use table data that contains location information.
-   **[Create a heatmap visualization in the Visualization Designer](../task/create-dv-heatmap-ac.md)**  
Use a heatmap visualization to show the relationship between two table fields or indicator breakdowns. The changes in color as you move along the axes reveal patterns in the value of one or both fields/breakdowns.
-   **[Create a horizontal or vertical bar data visualization](../task/create-dv-bar-ac.md)**  
Use bar visualizations to show information in segments that are proportional to the values they represent. Vertical bar and horizontal bar visualizations compare numeric values that represent either nominal or ordinal data.
-   **[Create a pie or donut visualization in the Visualization Designer](../task/create-dv-donut-ac.md)**  
Use pie, donut, and semi-donut visualizations to compare the size of parts of a data set to the whole. The segments of these charts should total to 100%.
-   **[Create a Pareto bar data visualization](../task/create-dv-pareto-vd.md)**  
Use a Pareto bar visualization to Identify the most important dimension in a large set of dimensions. Pareto bar visualization columns show data in descending order. A line shows the cumulative percentage.
-   **[Create a pivot table visualization in the Visualization Designer](../task/create-dv-pivot-ac.md)**  
Create a pivot table visualization to summarize large data sets by breaking them down by multiple dimensions in a single table. Cells show each row and column value combination and can also show subtotals.
-   **[Create time series visualizations](../task/create-dv-time-series-ac.md)**  
Show changes in data over time. Use different time series charts to emphasize different aspects of the data, such as trends or individual values.
-   **[Create a calendar report visualization in the Visualization Designer](../task/create-dv-calendar-ac.md)**  
Create calendar report visualizations to show and highlight date-driven events.
-   **[Create a simple list visualization in the Visualization Designer](../task/create-dv-simple-list-ac.md)**  
List reports display data in the form of an expandable list. For example, an incident report grouped by priority displays only the priority names and a number of records that display if the user selects the priority. You can configure whether lists display expanded or collapsed.
-   **[Create an Indicator Scorecard](../task/create-dv-indicator-scorecard.md#)**  
The Indicator Scorecard component enables users to visualize and compare data between multiple Performance Analytics indicators. It highlights the information regarding the last score collected, the change from the previous data point, the trend over time, and the value of the target to achieve.​
-   **[Create a data visualization from a list](../../par-for-workspace/task/create-data-viz-from-list.md)**  
You can create a Platform Analytics vertical bar or pie data visualization from inside a Core UI list. If you have a data visualization role, you can save, share, export, or duplicate the visualization.

**Parent Topic:**[Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md)

**Related topics**  


[Exploring the data visualization library](../../performance-analytics/concept/explore-data-vis-library.md)

[Common data visualization tasks](common-dv-tasks.md)

[View data visualizations](../../performance-analytics/concept/view-data-visualizations.md)

[Configure data visualizations](../../performance-analytics/concept/configure-data-visualizations.md)

[Data visualization reference](../../par-for-workspace/reference/data-visualization-reference.md)

