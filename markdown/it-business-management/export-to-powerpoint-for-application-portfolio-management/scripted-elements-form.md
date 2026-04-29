---
title: Scripted Elements form
description: Use the Scripted Elements form to define the data script to fetch data for a complex report type such as line chart or bar chart.
locale: en-US
release: australia
product: Export to PowerPoint for Application Portfolio Management
classification: export-to-powerpoint-for-application-portfolio-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Export to PowerPoint for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Scripted Elements form

Use the Scripted Elements form to define the data script to fetch data for a complex report type such as line chart or bar chart.

<table id="table_hwf_ymm_t5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the element.

</td></tr><tr><td>

Type

</td><td>

Chart type \(Line chart or Bar chart\) that you want to generate.After the required chart type is selected, the suggested format of the scripted elements code format is displayed in the **Data Script** field.

</td></tr><tr><td>

Description

</td><td>

Description for the report. \(Example: Comparison of planned vs. Actual costs.\)

</td></tr><tr><td>

Data Script

</td><td>

Script used to fetch data for the report.For more information on how to manage Scripted Elements, see [Manage Related Tables and Scripted Elements forms](../task/manage-components-export-ppt.md).

</td></tr></tbody>
</table>## Line chart parameter

Following are the basic parameters used to define the properties and formatting of a line chart.

<table id="table_mw2_1xz_qvb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Reference value

</th></tr></thead><tbody><tr><td>

`@property {String} seriesArray.properties.color - Color of Line`

</td><td>

Color of the line.

</td><td>

Use Hex code values to define a color of the line.

 For example, use the hex code `#FF0000` for red color.

</td></tr><tr><td>

`@property {String} seriesArray.properties.type - type of Line`

</td><td>

Type of line.

</td><td>

For more information about reference line formats, see [https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/PresetLineDash.html\#DASH](https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/PresetLineDash.html#DASH).

</td></tr><tr><td>

`@property {String} seriesArray.properties.markerStyle - style of marker`

</td><td>

Style of the marker to identify key points on the chart.

</td><td>

For more information about reference marker formats, see [https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/MarkerStyle.html](https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/MarkerStyle.html).

</td></tr><tr><td>

`@property {Number} seriesArray.properties.markerSize - size of style`

</td><td>

Size of the marker on the chart.

</td><td>

Minimum inclusive: 2, maximum inclusive: 72

</td></tr><tr><td>

`@property {String} legendPosition - Position of legend in chart. This is optional`

</td><td>

Legend position of the chart.

</td><td>

For more information about legend position, see [https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/LegendPosition.html](https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/LegendPosition.html).

</td></tr></tbody>
</table>## Bar chart parameters

Following are the basic parameters used to define the properties and formatting of a bar chart.

<table id="table_jmc_gyz_qvb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Reference value

</th></tr></thead><tbody><tr><td>

`@property {String} barProperties.direction`

</td><td>

The direction of plotting the bars in the chart.

</td><td>

For more information about defining a bar direction, see [https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/BarDirection.html](https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/BarDirection.html).

</td></tr><tr><td>

`@property {String} barProperties.grouping - grouping of bars`

</td><td>

Grouping style of the bar in the chart.

</td><td>

Use options such as standard, clustered, stack. For more information about bar grouping properties, see [https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/BarGrouping.html](https://poi.apache.org/apidocs/dev/org/apache/poi/xddf/usermodel/chart/BarGrouping.html).

</td></tr><tr><td>

`@property {Number} barProperties.overlay`

</td><td>

Size of overlapping among the bars in the chart.

</td><td>

Accepted numeric value range is from 0 to 100.

</td></tr></tbody>
</table>**Parent Topic:**[Export to PowerPoint Reference](export-ppt-reference.md)

