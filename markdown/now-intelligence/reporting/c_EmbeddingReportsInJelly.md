---
title: Embedding reports in Jelly
description: You can embed reports in any Jelly-based element, such as a UI page.When embedding a report in a Jelly element, you can define a report at any time by passing parameters.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Embedding reports in Jelly

You can embed reports in any Jelly-based element, such as a UI page.

## Enabling Embedding

To enable embedding reports in Jelly, add the following element to your Jelly code.

`<g:inline template="reporting_includes.xml" />`

After adding this code, you can embed an existing report, or generate a report within the Jelly code.

## Embedding an existing report

You can embed an existing report by calling the `embedReportById(targetSpan, reportId)` function.

For example, add the following to the HTML/XML block in the UI page record:

```
<xml version="1.0" encoding="utf-8">
     <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
     <g:inline template="reporting_includes.xml" />
     <div id="report_stuff" />
     </j:jelly>

```

And add the following to the Client script block in the UI page record. Replace &lt;report sys\_id&gt; with the report's actual sys\_id:

```
var div = $j("#report_stuff");
embedReportById(div, <"report sys_id">);
```

Alternatively, you can embed the JavaScript in the jelly code entirely in the HTML/XML block. Add the code from the client script block between &lt;script&gt; tags:

```
<xml version="1.0" encoding="utf-8">
     <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
     <g:inline template="reporting_includes.xml" />
     <div id="report_stuff" />     
     <script>
          var div = $j("#report_stuff");
          embedReportById(div, <"report sys_id">);
     </script>
     </j:jelly>
```

|Parameter|Description|
|---------|-----------|
|targetSpan|The jQuery element to embed the chart in. The chart uses the size of this element.|
|reportId|The sys\_id of the report you want to embed.|

## Generate and embed a report

You can embed a report within the UI by calling the `embedReportByParams(targetSpan, parms)` function. When embedding a report in this way, you can generate a new report using parameters, or specify a report sys\_id to display that report.

For example, add the following to the HTML/XML block in the UI page record:

```
<xml version="1.0" encoding="utf-8">
     <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
     <g:inline template="reporting_includes.xml" />
     <div id="report_stuff" />
     </j:jelly>

```

And add the following to the Client script block in the UI page record:

```
var params = {sysparm_title: "Average for all ratings", sysparm_field: "category", sysparm_type: "bar", sysparm_table: "asmt_category_result", sysparm_aggregate: "AVG", sysparm_sumfield: "rating"}; 
var div = $j("#report_stuff");
embedReportByParams(div, params);
```

Alternatively, you can embed the JavaScript inside the jelly code. Add the code from the client script block between &lt;script&gt; tags:

```
<xml version="1.0" encoding="utf-8">
     <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
     <g:inline template="reporting_includes.xml" />
     <div id="report_stuff" />
     <script>
          var params = {sysparm_title: "Average for all ratings", sysparm_field: "category", sysparm_type: "bar", sysparm_table: "asmt_category_result", sysparm_aggregate: "AVG", sysparm_sumfield: "rating"};
          var div = $j("#report_stuff");
          embedReportByParams(div, params);
     </script>
     </j:jelly>

```

|Parameter|Description|
|---------|-----------|
|targetSpan|The jQuery element to embed the chart in.|
|parms|A JSON object defining the report. Available parameters depend on the report type.|

## Generating and embedding a list report

When you embed an existing list report or generate a list report and embed it, you must enter one more line of code.

Add the following to the HTML/XML block in the UI page record:

```
<xml version="1.0" encoding="utf-8">
     <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
     <g:inline template="reporting_includes.xml" />
     <g:inline template="list2_js_includes.xml" />  
     <div id="report_stuff" />
     </j:jelly>

```

Add the following to the Client script block in the UI page record. Replace &lt;report sys\_id&gt; with the report's actual sys\_id:

```
var div = $j("#report_stuff");
embedReportById(div, <"report sys_id">);
```

Or embed the JavaScript in the jelly code entirely in the HTML/XML block. Add the code from the client script block between &lt;script&gt; tags:

```
<xml version="1.0" encoding="utf-8">
     <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
     <g:inline template="reporting_includes.xml" />
     <g:inline template="list2_js_includes.xml" />
     <div id="report_stuff" />     
     <script>
          var div = $j("#report_stuff");
          embedReportById(div, <"report sys_id">);
     </script>
     </j:jelly>
```

|Parameter|Description|
|---------|-----------|
|targetSpan|The jQuery element to embed the chart in. The chart uses the size of this element.|
|reportId|The sys\_id of the report you want to embed.|

**Parent Topic:**[Advanced Core UI reporting topics](c_AdvancedReporting.md)

## Embedded report parameters

When embedding a report in a Jelly element, you can define a report at any time by passing parameters.

### Common parameters

Certain parameters are used by multiple report types.

<table id="table_pv4_ngr_cs"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

jvar\_report\_id

</td><td>

The sys\_id of a report record. If you pass this parameter, do not specify any other parameters. All values are taken from the report record.

</td><td>

 

</td></tr><tr><td>

sysparm\_report\_id

</td><td>

Use this parameter instead of jvar\_report\_id when you want to override any of the other sysparm parameters that exist in the report.

</td><td>

 

</td></tr><tr><td>

sysparm\_title

</td><td>

The title of the report.

</td><td>

 

</td></tr><tr><td>

sysparm\_table

</td><td>

The table to report on. Specify this value or sysparm\_report\_source\_id, but not both.

</td><td>

 

</td></tr><tr><td>

sysparm\_report\_source\_id

</td><td>

The sys\_id of a report source. Specify this value or sysparm\_table, but not both. This value is used instead of sysparm\_table if you pass both.

</td><td>

 

</td></tr><tr><td>

sysparm\_type

</td><td>

The type of report to create. Possible values: list, line, line\_bar, area, spline, bar, horizontal\_bar, pareto, hist, pie, donut, semi\_donut, speedometer, dial, pivot, pivot\_v2, funnel, calendar, pyramid, box, trend, control, trendbox, and heat map.

</td><td>

line

</td></tr><tr><td>

sysparm\_field

</td><td>

The field from the specified table to group data by. Required for time series, column, bar, pie, donut, funnel, pyramid, box, trend, and trendbox reports. Optional for list reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_query

</td><td>

The filter to apply to the data before generating the report. Specify a query string for this value. To sort your query results by a specific field, add `^ORDERBY<field_name>` or `^ORDERBYDES<field_name>` to the end of the query string. ORDERBY sorts the query by ascending order. ORDERBYDES sorts the query by descending order.

</td><td>

 

</td></tr><tr><td>

sysparm\_aggregate

</td><td>

The aggregation type.Possible values: AVG, COUNT, SUM, and COUNT\_DISTINCT

</td><td>

COUNT

</td></tr><tr><td>

sysparm\_sumfield

</td><td>

The field to aggregate data on. This parameter does not apply when using a COUNT aggregation type.

</td><td>

 

</td></tr><tr><td>

sysparm\_display\_grid

</td><td>

A true/false value that controls whether the report displays a data grid.

</td><td>

false

</td></tr><tr><td>

sysparm\_show\_other

</td><td>

A true/false value that controls whether the Other group appears on the report. This group appears only if the number of groups exceeds the number specified in the sysparm\_others parameter. This parameter applies to bar, pie, funnel, pyramid, pivot, and heat map reports.

</td><td>

true

</td></tr><tr><td>

sysparm\_others

</td><td>

The maximum number of individual groups of data to display. Any additional data groups are combined into the Other group. This parameter applies to bar, pie, funnel, pyramid, pivot, and heat map reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_source\_type

</td><td>

The source of the embedded report. Optional.Possible values: table, metricbase, source, import

</td><td>

table

</td></tr><tr><td>

sysparm\_set\_color

</td><td>

The color setting for the report.Possible values: one\_color, color\_palette, several\_colors

</td><td>

color\_palette

</td></tr><tr><td>

sysparm\_color\_palette

</td><td>

The color palette that the report uses. This parameter is used when sysparm\_set\_color="color\_palette".Possible value: The sys\_id of a color palette

</td><td>

Default UI14

</td></tr><tr><td>

sysparm\_color

</td><td>

The color that the report uses. This parameter is used when sysparm\_set\_color="one\_color".Possible value: The sys\_id of a color

</td><td>

 

</td></tr><tr><td>

sysparm\_chart\_colors

</td><td>

The set of chart colors that the report uses. This parameter is used when sysparm\_set\_color="several\_colors".Possible value: A comma-separated list of color hex codes

</td><td>

 

</td></tr><tr><td>

sysparm\_show\_marker

</td><td>

A marker is the value represented by a dot in a line or another graphic element in a chart. This parameter is a true/false value that controls whether the marker appears.

</td><td>

true

</td></tr><tr><td>

sysparm\_show\_empty

</td><td>

A true/false value that controls if records with empty grouping or trend values appear on the report.

</td><td>

false

</td></tr><tr><td>

sysparm\_stack\_field

</td><td>

The field used to control stacking on bar and column reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_bar\_unstack

</td><td>

A true/false value that controls if stacked data is presented as a single bar or column, or as multiple bars.

</td><td>

false

</td></tr><tr><td>

sysparm\_box\_field

</td><td>

The numeric field used to measure the data. This parameter is required for box and histogram reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_trend\_field

</td><td>

The date-time field used to organize trend data. This parameter is required for time series, trend, and box reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_trend\_interval

</td><td>

The interval to measure trend values by. Possible values: year, quarter, month, week, dayofweek, hour, and date.

</td><td>

year

</td></tr><tr><td>

sysparm\_compute\_percent

</td><td>

The value to use when displaying report percentages. You can display percentages based on the total record count, or by the specified aggregate.Possible values: aggregate and count

</td><td>

count

</td></tr><tr><td>

sysparm\_funnel\_neck\_percent

</td><td>

A number 1–100 that defines the percentage of a funnel report that is the neck of the funnel.

</td><td>

30

</td></tr><tr><td>

sysparm\_show\_chart\_data\_label

</td><td>

A true/false value that controls if data labels appear on the report.

</td><td>

false

</td></tr><tr><td>

sysparm\_show\_zero

</td><td>

A true/false value that controls if zeroes appear on multilevel pivot and heat map reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_ct\_row

</td><td>

The field used to define the rows in heat map and bubble reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_ct\_column

</td><td>

The field used to define the columns in heat map and bubble reports.

</td><td>

 

</td></tr><tr><td>

sysparm\_y\_axis\_category\_fields

</td><td>

The field used to define the rows in multilevel pivot reports. Specify up to five comma-separated field names.

</td><td>

 

</td></tr><tr><td>

sysparm\_x\_axis\_category\_fields

</td><td>

The field used to define the columns in multilevel pivot reports. Specify up to three comma-separated field names.

</td><td>

 

</td></tr><tr><td>

sysparm\_list\_ui\_view

</td><td>

The sys\_id of a list view to use when a user drills into the report.

</td><td>

 

</td></tr><tr><td>

sysparm\_show\_marker

</td><td>

A true/false value that controls if markers appear at every plotted point on a report.

</td><td>

true

</td></tr><tr><td>

sysparm\_apply\_alias

</td><td>

A true/false value that controls if configured aliases appear in embedded reports.

</td><td>

 

</td></tr></tbody>
</table>### Service catalog parameters

Certain parameters apply only to reports created on service catalog tables, such as the Requested Item \[sc\_req\_item\] table. These parameters are not available on list or calendar type reports.

|Parameter|Description|
|---------|-----------|
|sysparm\_sc\_groupby\_item\_id|The sys\_id of a catalog item. Use this parameter with the **sysparm\_sc\_groupby\_variable\_id** parameter to group a service catalog report based on a catalog variable value. These parameters replace the**sysparm\_field** parameter when grouping on service catalog variables.|
|sysparm\_sc\_groupby\_variable\_id|The sys\_id of the catalog item variable used to determine how data is grouped on the report. This variable must belong to the catalog item specified in the **sysparm\_sc\_groupby\_item\_id**parameter.|
|sysparm\_sc\_stackby\_item\_id|The sys\_id of a catalog item. Use this parameter with the**sysparm\_sc\_stackby\_variable\_id** parameter to stack a service catalog report based on a catalog variable value. These parameters replace the **sysparm\_stack\_field** parameter when grouping on service catalog variables. Only reports that support stacking, such as bar reports, support these parameters.|
|sysparm\_sc\_stackby\_variable\_id|The sys\_id of the catalog item variable used to determine how data is grouped on the report. This variable must belong to the catalog item specified in the **sysparm\_sc\_stackby\_item\_id**parameter.|

### MetricBase parameters

To use MetricBase in an embedded report, the sysparm\_source\_type parameter must be set to "metricbase".

MetricBase also requires the sysparm\_custom\_configuration parameter, which has the following syntax:

```
sysparm_custom_config: "{query_condition:\"\",transforms:[{transform:{transform:\"Reference\",name:\"chart-subjects\"},metric:\"mb_metricname\"}], group_by:\"\", table:\"mb_tablename\"}"; 
```

In this syntax:

-   A `transform` is a chain of nested transform functions. The last transform of every chain must always be the Reference transform:

    ```
    {transform:\"Reference\",name:\"chart-subjects\"}
    ```

-   A `metric` is a metric field of a metric table.
-   The `group-by` field is the field on the selected metric table by which the time series is grouped.
-   `table` refers to the metric table
-   `mb_...` are placeholder names

All attributes are required except for `group-by`.

### Chart-specific parameters

Certain parameters are available only for specific report types.

|Parameter|Description|Default value|
|---------|-----------|-------------|
|sysparm\_show\_chart\_total|A true/false value that controls if the total score of the grouped donut appears in the center of the report.|false|
|sysparm\_donut\_width\_percent|A number 1–100 that controls the thickness of the donut report.|50|

|Parameter|Description|Default value|
|---------|-----------|-------------|
|sysparm\_use\_color\_heatmap|A true/false value that controls if the heatmap uses a gradient to color the report. When true, the sysparm\_axis\_max\_color and sysparm\_axis\_min\_color values are used.|true|
|sysparm\_axis\_max\_color|The color used in the heatmap gradient to indicate a high value. This value must be the sys\_id of a Color Definition \[sys\_report\_color\] record.|UI14 blue|
|sysparm\_axis\_min\_color|The color used in the heatmap gradient to indicate a low value. This value must be the sys\_id of a Color Definition \[sys\_report\_color\] record.|white|

<table id="table_ycl_tgr_cs"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

sysparm\_gauge\_autoscale

</td><td>

A true/false value that controls if the dial automatically calculates the minimum and maximum scale on the report. If you set this value to false, you must specify a sysparm\_from and sysparm\_to value.

</td><td>

true

</td></tr><tr><td>

sysparm\_from

</td><td>

A number that defines the minimum value for the axis scale.

</td><td>

 

</td></tr><tr><td>

sysparm\_to

</td><td>

A number that defines the maximum value for the axis scale.

</td><td>

 

</td></tr><tr><td>

sysparm\_upper\_limit

</td><td>

A number that defines the upper threshold for the dial. If you do not specify a value, the dial has no upper threshold.

</td><td>

 

</td></tr><tr><td>

sysparm\_lower\_limit

</td><td>

A number that defines the lower threshold for the dial. If you do not specify a value, the dial has no lower threshold.

</td><td>

 

</td></tr><tr><td>

sysparm\_direction

</td><td>

A value that controls which values are considered positive on the report, lower values or higher values. Possible values: minimize and maximize.

</td><td>

minimize

</td></tr></tbody>
</table>### Chart size parameters

Certain parameters control the width and height of the report.

|Parameter|Description|Default value|
|---------|-----------|-------------|
|sysparm\_chart\_size|The size of the chart in the report. Valid values are small, medium, and large.|large|
|sysparm\_custom\_chart\_size|Enable this parameter to specify custom chart height and width values instead of using a size option from the **sysparm\_chart\_size** parameter.|false|
|sysparm\_custom\_chart\_height|The height of the chart in the report, in pixels.| |
|sysparm\_custom\_chart\_width|The width of the chart in the report, in pixels.| |

### Chart title parameters

Certain parameters are available only for reports that display a title. These report types include time series, bar, column, pie, donut, dials, trend, box, trend box, histogram, pyramid, heat map, funnel, and control reports.

<table id="table_ml1_rhr_cs"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

sysparm\_report\_title\_size

</td><td>

A number that defines the font size of the title.

</td><td>

16

</td></tr><tr><td>

sysparm\_report\_title\_color

</td><td>

The title text color. This value must be the sys\_id of a Color Definition \[sys\_report\_color\] record.

</td><td>

black

</td></tr><tr><td>

sysparm\_title\_horizontal\_alignment

</td><td>

Where the title is placed horizontally relative to the report. This value is used only if sysparm\_custom\_report\_title\_position is false.Possible values are: left, center, and right.

</td><td>

center

</td></tr><tr><td>

sysparm\_title\_vertical\_alignment

</td><td>

Where the title is placed vertically relative to the report. This value is used only if sysparm\_custom\_report\_title\_position is false.Possible values: top, middle, and bottom.

</td><td>

top

</td></tr><tr><td>

sysparm\_custom\_report\_title\_position

</td><td>

A true/false value that controls whether the x and y coordinates define the report title position instead of relative alignment.

</td><td>

false

</td></tr><tr><td>

sysparm\_report\_title\_x\_position

</td><td>

A number that defines the x position of the title on the report. This value is used only if sysparm\_custom\_report\_title\_position is true.

</td><td>

0

</td></tr><tr><td>

sysparm\_report\_title\_y\_position

</td><td>

A number that defines the y position of the title on the report. This value is used only if sysparm\_custom\_report\_title\_position is true.

</td><td>

0

</td></tr></tbody>
</table>### Chart border parameters

Certain parameters are available only for reports that display a border. These report types include: time series, bar, column, pies, donuts, dials, trend, box, trend box, histogram, pyramid, heat map, funnel, and control reports.

|Parameter|Description|Default value|
|---------|-----------|-------------|
|sysparm\_show\_report\_border|A true/false value that controls whether the report displays a border.|false|
|sysparm\_report\_border\_width|A number that defines the width of the border, in pixels.|1|
|sysparm\_report\_border\_radius|A number that defines the radius size of the corners of the border, in pixels.|0|

### Legend parameters

Certain parameters are available only for reports that display a legend. These report types include pie, donut, stacked bar, stacked column, time series, trend, box, histogram, pyramid, control, and heat map reports.

<table id="table_mrs_thr_cs"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

sysparm\_show\_legend

</td><td>

A true/false value that controls whether the report displays a legend.

</td><td>

true

</td></tr><tr><td>

sysparm\_legend\_horizontal\_alignment

</td><td>

Where the legend is placed horizontally relative to the report.Possible values: left, center, and right.

</td><td>

center

</td></tr><tr><td>

sysparm\_legend\_vertical\_alignment

</td><td>

Where the legend is placed vertically relative to the report.Possible values: top, middle, and bottom.

</td><td>

bottom

</td></tr><tr><td>

sysparm\_show\_legend\_border

</td><td>

A true/false value that controls whether the legend displays a border.

</td><td>

true

</td></tr><tr><td>

sysparm\_legend\_border\_width

</td><td>

A number that defines the width of the legend border, in pixels.

</td><td>

1

</td></tr><tr><td>

sysparm\_legend\_border\_radius

</td><td>

A number that defines the radius size of the corners of the legend border, in pixels.

</td><td>

0

</td></tr></tbody>
</table>### X-axis parameters

Certain parameters are available only for reports that use an X axis. These report types include bar, horizontal bar, pareto, column, line area, spline, box, trendbox, control, and trend reports.

|Parameter|Description|Default value|
|---------|-----------|-------------|
|sysparm\_x\_axis\_title|The name to display on the x axis.| |
|sysparm\_x\_axis\_title\_size|A number that defines the font size of the x-axis title.| |
|sysparm\_x\_axis\_title\_bold|A true/false value that controls whether the x-axis title text is bold.|true|
|sysparm\_x\_axis\_opposite|A true/false value that controls if the x axis appears at the top of the report.|false|
|sysparm\_x\_axis\_display\_grid|A true/false value that controls if vertical grid lines appear from the x axis.|false|
|sysparm\_x\_axis\_grid\_dotted|A true/false value that controls whether the vertical grid lines are dotted.|false|
|sysparm\_x\_axis\_label\_size|A number that defines the font size for increment labels on the x axis.|11|
|sysparm\_x\_axis\_label\_bold|A true/false value that controls whether the x-axis increment labels are bold.|false|

### Y-axis parameters

Certain parameters are available only for reports that use a Y axis. These report types include bar, horizontal bar, Pareto, column, line area, spline, box, trendbox, control, and trend reports.

|Parameter|Description|Default value|
|---------|-----------|-------------|
|sysparm\_y\_axis\_title|The name to display on the y axis.|An automatically generated description of the report aggregation|
|sysparm\_y\_axis\_title\_size|A number that defines the font size of the y-axis title.| |
|sysparm\_y\_axis\_title\_bold|A true/false value that controls whether the y-axis title text is bold.|true|
|sysparm\_y\_axis\_opposite|A true/false value that controls if the y axis appears on the left of the report.|false|
|sysparm\_y\_axis\_display\_grid|A true/false value that controls if horizontal grid lines appear from the y axis.|true|
|sysparm\_y\_axis\_grid\_dotted|A true/false value that controls whether the horizontal grid lines are dotted.|false|
|sysparm\_y\_axis\_label\_size|A number that defines the font size for increment labels on the y axis.|12|
|sysparm\_y\_axis\_label\_bold|A true/false value that controls whether the y-axis increment labels are bold.|false|
|sysparm\_y\_axis\_from|A number defining the lowest value displayed on the y axis.| |
|sysparm\_y\_axis\_to|A number defining the highest value displayed on the y axis.| |

