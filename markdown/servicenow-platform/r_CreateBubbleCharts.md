---
title: Create a bubble chart
description: Assessment administrators can create bubble charts to compare the relative standing of assessable records in three metric categories.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [View a bubble chart for assessments, View a metric result, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a bubble chart

Assessment administrators can create bubble charts to compare the relative standing of assessable records in three metric categories.

To create a bubble chart, navigate to **Assessments** &gt; **Admin** &gt; **Bubble Charts** and create a record \(see table for field descriptions\).

**Note:** For color fields, either HTML [color names](http://www.w3.org/TR/css3-color/#svg-color) or [hexadecimal](http://www.w3schools.com/tags/ref_colorpicker.asp) \(hex\) values are acceptable. For hex values, the \# character is optional. Values are not case-sensitive. For example, all of the following values are valid: LightGray, lightgray, \#D3D3D3, d3d3d3.

![Bubble chart](../image/BubbleChartForm.png "Bubble Chart form")

<table id="table_klm_lsl_lt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the bubble chart. **Bubble Chart** is appended to the name when you view the bubble chart.

</td></tr><tr><td>

-   Top left label
-   Top right label
-   Bottom left label
-   Bottom right label

</td><td>

Label text for the top left, top right, bottom left, and bottom right quadrants, respectively. Choose labels that help interpret results. For example, a bubble chart that displays vendor assessment results might have the following quadrant labels, where vendors in the top right quadrant have the best scores: -   **Top left label**: Resource
-   **Top right label**: Essential Partner
-   **Bottom left label**: Poor Performer
-   **Bottom right label**: Reevaluate

</td></tr><tr><td>

-   Top left color
-   Top right color
-   Bottom left color
-   Bottom right color

</td><td>

Border colors for the top left, top right, bottom left, and bottom right quadrants, respectively. Bubbles are the color of the quadrant they are in.

</td></tr><tr><td>

Type

</td><td>

Metric type associated with this bubble chart. Only results for assessable records of the selected metric type are plotted on the bubble chart.

</td></tr><tr><td>

-   X-Axis label
-   Y-Axis label
-   Z-Axis label

</td><td>

Label text for the X-, Y-, and Z-axis categories of the bubble chart. These labels appear along the X- and Y-axes, if applicable, and in bubble score summary windows. The metric category name is usually a good label. If these fields are left empty, the bubble chart automatically displays the selected category names as the labels.

</td></tr><tr><td>

-   Metric X category
-   Metric Y category
-   Metric Z category

</td><td>

Metric category each axis represents. Results for the Z-axis category determine the size of each bubble. The Z-axis should generally represent the most important category out of the three.

</td></tr><tr><td>

Quadrant label color

</td><td>

Color of the label text for the quadrant borders.

</td></tr><tr><td>

Default

</td><td>

Check box that enables \(selected\) or disables \(cleared\) the bubble chart as the default. There can be only one default bubble chart per metric type.

</td></tr></tbody>
</table>**Parent Topic:**[View a bubble chart for assessments](../task/t_view-bubble-chart-assessments.md)

