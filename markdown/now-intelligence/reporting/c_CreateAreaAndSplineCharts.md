---
title: Area and spline reports
description: Area reports show trends over time for related attributes. Spline reports show how one or more values change over time by connecting a series of known data points with a curve that emphasizes the trend over individual data points.Create an area or spline report to show trends over time for related attributes.Change the look of your area or spline report.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 19
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Area and spline reports

Area reports show trends over time for related attributes. Spline reports show how one or more values change over time by connecting a series of known data points with a curve that emphasizes the trend over individual data points.

For example, you can create an area or spline reports for incident counts, to show how the number of incidents changes over time. The incident count often increases during the first few months after a product upgrade is deployed. Over time, the number of reported incidents decreases as users become more accustomed to the changes in the product.

**Note:** This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see [Time series visualization type use cases](../reference/time-series-visualization-types.md).

![Area reports](../image/AreaChart.png "Area reports")

**Note:**

When the sections of an area report with multiple datasets overlap, it is not possible to drill down into the various sections. To drill down, click items in the legend to clear them from the report.

![Spline report](../image/SplineChart.png "Spline report")

**Note:** This data visualization is supported on the mobile platform. For more information, see [Time series reports for mobile](https://www.servicenow.com/docs/access?context=mobile-reporting-time-series&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US) and [Mobile dashboard preview](https://www.servicenow.com/docs/access?context=mobile-dashboard-preview&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).

## Create an area or spline report

Create an area or spline report to show trends over time for related attributes.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

For an area report use case, [Time series visualization example](../../par-for-workspace/task/dv-example-line.md).

### Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d95393e249">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d95393e268">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td id="d95393e287">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d95393e312">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select **Next**.

5.  On the **Type** tab, enter **Area** or **Spline** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

6.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_a5d_h2k_zw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group by

</td><td>

Group report data using the values of this field. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. To group by fields on extended tables, see [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#). Select the info icon \(![Info icon](../image/icon-info.png)\) for a description of the selected field. Configured function fields appear in this list after you save the report.

 **Note:**

-   It is not possible to group or stack reports by the **Tags** field, or by certain MySQL database field types, such as MEDIUMTEXT. For more information, see [Database field type](https://www.servicenow.com/docs/access?context=r_DatabaseFieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Grouping or stacking by Variables or Questions fields is not supported for reports based on [database views](../../performance-analytics/concept/performance-analytics-glossary.md#).


</td></tr><tr><td>

Additional group by

</td><td>

Extra fields to group the report by. When you select **Additional group by** fields or function fields, the report includes a control at the bottom that allows you to group the report by any one of the additional fields. To group by fields on extended tables as well, see [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#). Click the info icon \(![Info icon](../image/icon-info.png)\) for descriptions of the selected fields Configured function fields appear in this list after you save the report.

**Note:**

-   You can see choices in the **Additional group by** list that do not appear in the main **Group by** list. The report does not support grouping or stacking by the extra fields you see. Unlike the main **Group by** choices, the **Additional group by** fields are not filtered. If you select an unsupported field, it has no effect.
-   The limitations listed for the main **Group by** field also apply to the **Additional group by** field.
 For more information, see [Add an additional group by or stack by](../task/add-additional-group-by-stack-by.md).

</td></tr><tr><td>

Display data table

</td><td>

Select this option to show report data in a list below the report. The list appears on dashboards where the report is added.All report visualizations show the report data when the [glide.ui.section508](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) system property is set to **true**. The glide.ui.section508 property overrides the **Display data table** field.

</td></tr><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Trend by

</td><td>

Table field whose values you want to show in a time sequence. Select the info icon \(![Info icon](../image/icon-info.png)\) for a description of the selected field. **Note:** If you selected a remote table in the **Table** field, the option you select in this field aggregates the data that was retrieved from an external source and aggregated in memory. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td>

Calendar

</td><td>

Calendar that is the basis for the time series in the report. Select either the standard calendar or a [customized business calendar](https://www.servicenow.com/docs/access?context=business-calendars&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

per

</td><td>

Time period to group data by. The range of available time periods depends on the calendar that you selected. Time periods range from an hour to a year. You can also specify a date.**Note:** If reporting per week: When the report range includes more than one calendar year, inconsistencies result when a week is split between two years. To show data values more accurately according to ISO weeks, add and enable the **glide.db.aggregates.trend.use\_iso\_week** property in the System Properties \[sys\_properties\] table.

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

Percentage calculation

</td><td>

Method of calculating percentages. The percentage appears when you point to a report segment, such as a bar on a bar report. This field appears when **Aggregation** is set to **Average**, **Sum**, or **Count Distinct**.

 -   **Use Aggregation** calculates the percentage using the selection in the **Aggregation** field. Only data that is displayed in the report is used to calculate the percentage.

For example, a report shows assets by department with the **Aggregation** set to **Sum** and the percentage calculated using aggregation. If the total cost of assets is $100,000 and the cost of assets for Customer Support is $10,000, the percentage for Customer Support is 10%.

-   **Use Record Count** calculates the percentage using the total number of records in the data set.

For example, a report shows incidents by priority. Out of 500 incident records, 200 have low priority. The percentage for the low-priority section is 40%.

</td></tr><tr><td>

Set Value Formatting

</td><td>

Enables you to configure how to show numerical values in reports, including decimal precision, rounding, minimum and maximum duration units, and abbreviations for duration units. See [Value formatting in reports](../reference/value-formatting-reports.md#).

 **Note:** Decimal precision does not work on currency fields.

</td></tr></tbody>
</table>7.  Configure the sort order of the applicable fields in the report \(column, row, Group by, Stack by or Trend by depending on the report type\).

    Select the filter icon \(![Filter icon for lists](../../../common/image/List_FilterIcon.png)\) and choose **Add Sort**.

    1.  In the Sorting Order list, choose the field you want to sort on and then choose **a-z** or **z-a** for alphabetical order or reverse alphabetical order.

        The list contains all possible fields from the report's source and fields on extended, or related, tables. The only effective values, however, are the fields chosen for the current report \(column, row, Group by, Stack by, or Trend by depending on the report type\).

        **Note:** On fields from dot-walked \(extended\) tables, you can only sort on date fields.

    2.  Select the sort plus icon \(![Sort plus icon](../image/sort-order-plus-icon.png)\) to configure additional sorting order conditions. \(Select the sort minus icon \( ![Sort minus icon](../image/sort-order-minus-icon.png)\) to delete configured sorting order conditions.\)
    3.  Select **Save**.
    For fields of the type Choice list, sort order is not determined alphabetically based on Label, it is sorted based on the **Value** of the choice field. For multi-level pivot table and heatmap reports, sort order is determined by the sequence of the choices in the list.

    ![Report sorted by priority choice list](../image/choice-list-sort-order.png)

8.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

10. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

## Area and spline report style options

Change the look of your area or spline report.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

<table id="table_wp4_4fb_wr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Chart color

</td><td>

Source of colors used in the report.If you do not group or stack the report, **Use one color** is automatically selected. In this case, select a single, predefined system color.

 If you group or stack the report, select one of the following options:

-   **Use color palette**: Select a color palette from the predefined system color palettes.
-   **Use several colors**: Define a custom set of **Colors** using hex codes. You can add any number of colors.
-   **Use chart colors**: Use the colors defined in **Reports** &gt; **Chart Colors**.

 For more information about the differences between these options, see [Predefined colors in reports](colors-reports.md).

</td></tr><tr><td>

Set color

</td><td>

Color used in the report. This field displays when you select **Use one color** from the **Chart color** list. Click the search icon \(![Search icon](../image/SearchIcon.png)\) to choose from the **Color Definitions** list.

</td></tr><tr><td>

Colors

</td><td>

Colors used in the report. This field displays when you select **Use several colors** from the **Chart color** list. Click the search icon \(![Search icon](../image/SearchIcon.png)\) to choose from the **Chart color schemes** or **Color Definitions** list.

</td></tr><tr><td>

Set palette

</td><td>

Color palette used in the report. This field appears when you select **Use color palette** from the **Chart color** list.

</td></tr><tr><td>

Display data labels

</td><td>

Check box to show the value for each data point.

</td></tr><tr><td>

Do not plot nil as zero

</td><td>

Check box to specify whether to replace missing data points with values of zero. This field is available when creating or editing time series reports \(area, spline, line, and step line reports only\) that include multiple datasets, and when creating or editing datasets within the applicable time series reports. This field is not available when data in the report is grouped, or is aggregated by Count or Count Distinct. If selected, the report may show gaps where no data exists.

**Note:** This property cannot be selected when the source is MetricBase.

</td></tr><tr><td>

Show marker

</td><td>

Check box to show a symbol at each data point.

</td></tr><tr><td>

Custom chart size

</td><td>

Check box to specify the width and height of the report in pixels.**Note:** The chart size is ignored when you export the report to PDF. In PDFs, the full page width is used to show the chart.

</td></tr><tr><td>

Chart size

</td><td>

Chart size. This field is available when **Custom chart size** is cleared. Options are **Small**, **Medium**, and **Large**.**Note:** The chart size is ignored when you export the report to PDF. In PDFs, the full page width is used to show the chart.

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

</td></tr><tr><td class="sub-head" colspan="2">

Legend

</td></tr><tr><td>

Show legend

</td><td>

Check box to show a chart legend. This check box appears when a **Group by** field is selected on the report form.Legends are truncated by default. To adjust truncation lengths, configure the properties **glide.chart.label.legend.truncate\_to** and **glide.chart.label.legend.truncate\_to.large**. For more information, see [Reporting properties](../reference/reporting-properties.md).

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

Check box to show a border around the legend. This check box appears when **Show legend** is selected.

</td></tr><tr><td>

Left align legend text

</td><td>

Check box to left-align the legend text when the report is viewed in a browser. By default, the legend text is centered. When the report is exported to PDF, PNG, or JPG, the legend remains centered. This check box appears when **Show legend** is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Axis

</td></tr><tr><td>

Y axis and X axis

</td><td>

Axis to configure the titles, appearance, and labels for.

</td></tr><tr><td>

Title

</td><td>

Title for the axis.

</td></tr><tr><td>

Title size

</td><td>

Size of the axis title in pixels. Default value is 12.

</td></tr><tr><td>

Title bold

</td><td>

Check this box to show the axis title in a bold typeface.

</td></tr><tr><td>

Opposite

</td><td>

On the **X axis** tab, select this check box to show the X-axis title on the right side of the report instead. On the **Y axis** tab, select this check box to show the Y-axis title on top of the report instead of across the bottom.

</td></tr><tr><td>

Display grid

</td><td>

On the **X axis** tab, select this check box to show horizontal grid lines on the report. On the **Y axis** tab, select this check box to show vertical grid lines on top the report.

</td></tr><tr><td>

Grid dotted

</td><td>

Check this box to show dotted grid lines instead of solid lines.

</td></tr><tr><td>

From

</td><td>

Specify a minimum Y-axis value to limit the amount of information in the report. If you select an aggregation field that is not of the type **Number**, the **From** and **To** fields are not available.**Note:**

-   Depending on configured [Highcharts](https://api.highcharts.com/highcharts/yAxis.min) settings, the minimum value may be rounded up or down. If you require the settings that affect this changed, contact the administrator.
-   If you format duration fields additionally using **Set Value Formatting** from the Configure tab:
    -   Values entered in the **From**/**To** fields \(**Style** &gt; **Y axis** are in seconds. The visualization displays y-axis labels as the selected **Minimum/Maximum duration unit** \(**Configure** &gt; **Set Value Formatting**\), and returns data that falls within the From/To \(seconds\) values.
    -   Example: If you set the minimum and maximum duration unit to **Minute**, the visualization displays y-axis labels as minutes, and returns data which falls within the corresponding seconds values set in the From/To fields.

</td></tr><tr><td>

To

</td><td>

Specify a maximum Y-axis value to limit the amount of information in the report. If you select an aggregation field that is not of the type **Number**, the **From** and **To** fields are not available.**Note:**

-   Depending on configured [Highcharts](https://api.highcharts.com/highcharts/yAxis.min) settings, the minimum value may be rounded up or down. If you require the settings that affect this changed, contact the administrator.
-   If you format duration fields additionally using **Set Value Formatting** from the Configure tab:
    -   Values entered in the **From**/**To** fields \(**Style** &gt; **Y axis** are in seconds. The visualization displays y-axis labels as the selected **Minimum/Maximum duration unit** \(**Configure** &gt; **Set Value Formatting**\), and returns data that falls within the From/To \(seconds\) values.
    -   Example: If you set the minimum and maximum duration unit to **Minute**, the visualization displays y-axis labels as minutes, and returns data which falls within the corresponding seconds values set in the From/To fields.

</td></tr><tr><td>

X axis / Y axis label size

</td><td>

On the **X axis** tab, specify the size of the labels for the rows of the report. On the **Y axis** tab, specify the size of the labels for the columns in the report.

</td></tr><tr><td>

Label bold

</td><td>

Check this box to show the labels of the report in a bold typeface.

</td></tr></tbody>
</table>