---
title: Dial and speedometer reports
description: Dials and speedometers provide a real-time count for an indicator. These charts cannot contain comparison or historical data. You can configure colors to display at a glance that values are within specified ranges.Create a dial or speedometer to provide a real-time count for an indicator, with colors to indicate value ranges.Change the look of your dial or speedometer report.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Dial and speedometer reports

Dials and speedometers provide a real-time count for an indicator. These charts cannot contain comparison or historical data. You can configure colors to display at a glance that values are within specified ranges.

**Note:** This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see

-   [Create a dial visualization in the Visualization Designer](../task/create-dv-dial-ac.md)
-   [Create a gauge visualization in the Visualization Designer](../task/create-dv-gauge-ac.md)

.

Report creators often use red to indicate unacceptable value ranges. A low value for monthly sales is worse than a high value, but a low value for incident resolution times is better than a high value. You can configure red for low monthly sales values and red for high incident resolution values.

Dials and speedometers also have different appearances:

-   A speedometer shows numbers in the form of a round meter with a defined range.
-   A dial shows where a score falls across ranges on a half-circle dial.

![Angular report](../image/AngularGauge.png "Angular speedometer report")

![Solid dial report](../image/SolidGauge.png "Solid dial report")

**Parent Topic:**[Report types](../reference/report-types-creation-details-rd.md)

## Create a dial or speedometer report

Create a dial or speedometer to provide a real-time count for an indicator, with colors to indicate value ranges.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d172019e247">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d172019e266">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td id="d172019e285">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d172019e310">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select **Next**.

5.  On the **Type** tab, enter **Speedometer** or **Dial** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

6.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_p4s_mql_x4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Aggregation

</td><td>

Mathematical calculation to perform on the data. The default is **Count**, which shows the number of records selected.To show only unique records, select **Count Distinct**. For example, if you want a report on the distinct number of users who have one or more of the roles in a given list of roles. Users with more than one role would be counted twice unless you use **Count Distinct**.

 Select **Average**, **Sum**, or **Count Distinct**, to show a list of fields from the selected **Table**. Select a field to **Aggregate by** from this list. For example, if you select an integer field, such as **Priority**, the data is expressed as a decimal value number.

 If you choose **Average**,**Sum**, or **Count Distinct**, you may further be able to aggregate on fields from extended tables. See [How to report on extended tables.](../task/t_AccessFieldExtendedTable.md#)

 **Note:** For duration values, the unit of measurement displayed in the aggregation axis cannot be customized.

</td></tr></tbody>
</table>7.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

8.  On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

## Dial and speedometer report style options

Change the look of your dial or speedometer report.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

<table id="table_h1l_1jh_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Chart color \(dial chart only\)

</td><td>

A predefined system color for the dial.

</td></tr><tr><td>

Set color

</td><td>

Color used in the report. This field displays when you select **Use one color** from the **Chart color** list. Click the search icon \(![Search icon](../image/SearchIcon.png)\) to choose from the **Color Definitions** list.

</td></tr><tr><td>

Custom chart size

</td><td>

Check box to specify the width and height of the report in pixels.**Note:** The chart size is ignored when you export the report to PDF. In PDFs, the full page width is used to show the chart.

</td></tr><tr><td>

Chart width

</td><td>

Width of the report in pixels. The default value is 600. This field is available when **Custom chart size** is selected.

</td></tr><tr><td>

Chart height

</td><td>

Height of the report in pixels. The default value is 450.This field appears when **Custom chart size** is selected.

</td></tr><tr><td>

Chart size

</td><td>

Chart size. This field is available when **Custom chart size** is cleared. Options are **Small**, **Medium**, and **Large**.**Note:** The chart size is ignored when you export the report to PDF. In PDFs, the full page width is used to show the chart.

</td></tr><tr><td>

Direction

</td><td>

Choose whether lower or larger numbers are better. Select **Minimize** if lower numbers are better. Select **Maximize** if larger numbers are better. This setting works with **Lower Limit** and **Upper Limit**, which determine the colors for the areas in the dial or speedometer. -   Green indicates that the figures are acceptable.
-   Orange indicates that the figures have changed, but are still within the acceptable range.
-   Red indicates that the figures are not acceptable.

</td></tr><tr><td>

Lower limit

</td><td>

The lower threshold for color change on the dial or speedometer. If it uses only two colors, specify the same number for both lower and upper limits.

</td></tr><tr><td>

Upper limit

</td><td id="entry_qkw_sws_gz">

The upper threshold for color change on the dial or speedometer. If it uses only two colors, specify the same number for both lower and upper limits.For example, a dial contains a current score of 50 and **Dial Autoscale** is selected. The **Lower Limit** is set to 50 and **Upper Limit** is set to 100 and the direction is **Minimize**. The dial displays the area 0–50 in green, the area 50–100 in orange, and the area above 100 in red.

 If **Lower Limit** is set to 50, **Upper Limit** is set to 100 and the direction is **Maximize**, the colors are reversed.

 If no upper and lower limits have been set, no colors are used in the visualization. If you want to have only two section or colors, you can set the upper and lower limits to the same number.

</td></tr><tr><td>

Dial autoscale

</td><td>

Check box to automatically generate start and end values for the dial or speedometer based on the selected data.

</td></tr><tr><td>

From

</td><td>

Custom minimum value to display on the left side of the dial or speedometer. This field is available when **Dial Autoscale** is cleared.

</td></tr><tr><td>

To

</td><td>

Custom maximum value to display on the right side of the dial or speedometer. This field is available when **Dial Autoscale** is cleared.

</td></tr><tr><td>

Drilldown view

</td><td>

List view to show when a user selects a segment of a report for which no drilldown report type is specified. This view is also used when the user reaches the lowest drilldown level of a report. See [Configure the list layout](https://www.servicenow.com/docs/access?context=t_ConfigureTheListLayout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) . If you specify a **Report drilldown**, **Drilldown view** is ignored.For more information, see [Define a report drilldown](c_DrillingDownWithinReports.md#).

</td></tr><tr><td>

Decimal precision

</td><td id="decimalPrecisionEntry">

Number of decimal places to show. You can show from zero to four decimal places. Default value: 2. To change the default value, create the system property glide.chart.decimal.precision and specify the value. **Note:** Percentage labels do not change accordingly with the decimal precision specified.

 ![Decimal precision - Bar report](../image/DecimalPrecision-BarReport.png) ![Decimal precision - Donut report](../image/DecimalPrecision-DonutReport.png)

</td></tr><tr><td class="sub-head" colspan="2">

Title

</td></tr><tr><td>

Show chart title

</td><td>

When the chart title is shown for the report.-   **Never**: Never show the chart title.
-   **Report only**: Shows the chart title on reports.
-   **Always**: Shows the chart title on reports, dashboards, and landing pages.

</td></tr><tr><td>

Chart title

</td><td>

The chart title has a maximum length of 40 characters. If no title is entered, the report name is used for the title. This field appears when **Report only** or **Always** is selected from the **Show chart title** list.

</td></tr><tr><td>

Size of the chart title

</td><td>

Size of the chart title in pixels. This field appears when **Report only** or **Always** is selected from the **Show chart title** list.

</td></tr><tr><td>

Chart title color

</td><td>

Color of the chart title. This field appears when **Report only** or **Always** is selected from the **Show chart title** list.

</td></tr><tr><td>

Custom chart title position

</td><td>

Check box to specify X and Y coordinates for the position of the chart title. This field appears when **Report only** or **Always** is selected from the **Show chart title** list.

</td></tr><tr><td>

Chart title X position

</td><td>

Number of pixels to adjust the chart title position right or left. By default the title appears at the center top of the chart. To move the chart title to the right, enter a positive value. To move the title to the left, enter a negative value.This field appears only when **Custom chart title position** is selected.

</td></tr><tr><td>

Chart title Y position

</td><td>

Number of pixels to adjust the chart title position up or down. By default the title appears at the center top of the chart. To move up the chart title, enter a positive value. To move the chart title down, enter a negative value.This field appears only when **Custom chart title position** is selected.

</td></tr><tr><td>

Title horizontal alignment

</td><td>

How the chart title is aligned horizontally. This field is available when the **Custom chart title position** option is cleared.

</td></tr><tr><td>

Title vertical alignment

</td><td>

How the chart title is aligned vertically. This field appears when **Custom chart title position** is cleared.

</td></tr></tbody>
</table>