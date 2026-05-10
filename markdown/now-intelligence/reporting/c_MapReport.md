---
title: Map reports
description: Map reports display data on a map. You can display data as a geographical heatmap \( Map report icon \) or view specific data points \( The pin locations icon for map reports \).Create a map report to plot your data on geographical heatmap or with pin locations for specific data points.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Map reports

Map reports display data on a map. You can display data as a geographical heatmap \(![Map report icon](../image/MapReportHeatmapButton.png)\) or view specific data points \(![The pin locations icon for map reports](../image/MapPinLocationsButton.png)\).

Zoom in on a map to get a more detailed view. In heatmap mode, click any region on the map that contains data to drill down into its map.

**Note:** On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).

Save the map report to drill down into it. You cannot drill down into unsaved reports.

The lowest level of a map hierarchy can display only data points. Click data on this lowest level to see the data in list view, or in drill-down view if one has been configured.

## Limitations

-   Maps are not supported on Internet Explorer versions 7 and 8.
-   Map reports cannot be saved as images on Internet Explorer versions 7 to 9, Firefox versions 31 to 37, Safari 5, or all versions of the Edge browser. For best results, use Chrome to work with map reports.
-   Map reports cannot be exported as PDFs, but can be saved as images.
-   This report type cannot be run as a scheduled report.

![Map report example](../image/MapReportExample.png)

## Create a map report

Create a map report to plot your data on geographical heatmap or with pin locations for specific data points.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d210690e267">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d210690e286">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md)

</td></tr><tr><td id="d210690e305">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d210690e330">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/metricbase/metricbase.md).

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **Map** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_ubz_ns1_mv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display data table

</td><td>

Select this option to show report data in a list below the report. The list appears on dashboards where the report is added.All report visualizations show the report data when the [glide.ui.section508](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) system property is set to **true**. The glide.ui.section508 property overrides the **Display data table** field.

</td></tr><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Aggregation

</td><td>

Mathematical calculation to perform on the data. The default is **Count**, which shows the number of records selected.To show only unique records, select **Count Distinct**.

 Select **Average**, **Sum**, or **Count Distinct**, to show a list of fields from the selected **Table**. Select a field to **Aggregate by** from this list.

 If you group the report by a field and select an **Average** aggregate, you get the average of each group. If a Total value is shown, it is the average of these group averages, not of the individual field values.

 Select **Minimum** or **Maximum** to show the maximum or minimum value for each segment of the report.

 For more information on aggregation options, see [Aggregation in reporting](../reference/aggregation-reporting.md).

 If you choose **Average**,**Sum**, **Count Distinct**, **Minimum**, or **Maximum**, you may be able to aggregate on fields from extended tables. See [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#).

 For information about aggregating on FX currency values, see [FX Currency values in reporting](fx-currency-values-reporting.md#).

</td></tr><tr><td>

Map this data

</td><td>

The data that you want to plot on the map. Only data that a report administrator has prepared as a map source is available.

</td></tr><tr><td>

Set map

</td><td>

The starting map for the report. You can zoom in but cannot zoom out from this map.

</td></tr></tbody>
</table>8.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  On the **Style** tab, configure the appearance of the report.

    Fill in the fields as appropriate.

<table id="table_h5j_tx4_bs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Use heatmap colors

</td><td>

Check box to use different colors to indicate different values on the map. If you clear this check box, all geographical locations with data are displayed in the same color.

</td></tr><tr><td>

Color for high scores

</td><td>

Color to indicate high values.

</td></tr><tr><td>

Color for low scores

</td><td>

Color to indicate low values.

</td></tr><tr><td>

Display data labels

</td><td>

Check box to show the value for each data point.

</td></tr><tr><td>

Display geographical labels

</td><td>

Check box to display the names of geographical objects on the map, such as countries, regions, and states.

</td></tr><tr><td>

Custom chart size

</td><td>

Enable the option to specify the width and height of the report in pixels.**Note:** The chart size is ignored when you export the report to PDF. In PDFs, the full page width is used to show the chart.

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

Drilldown view

</td><td>

List view to show when a user selects a segment of a report for which no drilldown report type is specified. This view is also used when the user reaches the lowest drilldown level of a report. See [Configure the list layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-administration/t_ConfigureTheListLayout.md) . If you specify a **Report drilldown**, **Drilldown view** is ignored.For more information, see [Define a report drilldown](c_DrillingDownWithinReports.md#).

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

</td></tr><tr><td class="sub-head" colspan="2">

Legend tab fields \(available only when colors are used on the report\)

</td></tr><tr><td>

Show legend

</td><td>

Enable this option to show a chart legend. This check box appears when a **Group by** field is selected on the report form.Legends are truncated by default. To adjust truncation lengths, configure the properties **glide.chart.label.legend.truncate\_to** and **glide.chart.label.legend.truncate\_to.large**. For more information, see [Reporting properties](../reference/reporting-properties.md).

</td></tr><tr><td>

Legend horizontal alignment

</td><td>

How the legend is aligned horizontally. This field appears when **Show legend** is selected.

</td></tr><tr><td>

Legend vertical alignment

</td><td>

How the legend is aligned vertically. This field appears when **Show legend** is selected.

</td></tr><tr><td>

Show legend border

</td><td>

Enable this option to show a border around the legend. This check box appears when **Show legend** is selected.

</td></tr><tr><td>

Left align legend text

</td><td>

Enable this option to left-align the legend text when the report is viewed in a browser. By default, the legend text is centered. When the report is exported to PDF, PNG, or JPG, the legend remains centered. This check box appears when **Show legend** is selected.

</td></tr></tbody>
</table>10. To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

11. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can share the report with users and groups, add the report to a dashboard, and publish the report to the web.

