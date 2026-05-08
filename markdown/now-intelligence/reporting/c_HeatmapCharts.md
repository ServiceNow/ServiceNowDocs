---
title: Heatmap reports
description: Heatmap reports display aggregate data visually using colors to represent different values on a matrix. Heatmap reports can have no more than 1000 cells.Create a heatmap report to show aggregate data visually using colors to represent different values on a matrix.Change the look of your heatmap chart.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Heatmap reports

Heatmap reports display aggregate data visually using colors to represent different values on a matrix. Heatmap reports can have no more than 1000 cells.

**Note:** When accessibility is enabled, this visualization includes a report that screen readers can interpret. For more information, see [Enabling accessibility features](https://www.servicenow.com/docs/access?context=c_SetUpSect508ComplianceFeature&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).

In the figure, the cell for confirmed low priority problems is filled to highlight the large value.![A heatmap report](../image/heatmapExample.png)

**Parent Topic:**[Report types](../reference/report-types-creation-details-rd.md)

## Create a heatmap report

Create a heatmap report to show aggregate data visually using colors to represent different values on a matrix.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### About this task

**Note:** A smaller-sized heatmap chart doesn't display non-zero values which would otherwise overlap an adjacent value. Row labels for these values also do not show. You can hover over a blank value cell to see its value, or enlarge the chart size to accommodate values. Understanding how this particular chart type behaves can help you interpret results and determine the appropriate sizing for your data.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d223359e216">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d223359e235">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td id="d223359e254">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d223359e279">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  On the **Type** tab, enter **Heatmap** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

5.  Fill in the fields, as appropriate \(see table\).

<table id="table_b1w_sh4_bs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Row

</td><td>

Field used as the source of the data for the rows in the heatmap. To select a source field on an extended table, see [How to report on extended tables.](../task/t_AccessFieldExtendedTable.md#) Select the info icon ![](../../par-for-workspace/image/icon-info.png) for a description of the selected field.

**Note:** Label names longer than 20 characters may show or print a truncated view.

</td></tr><tr><td>

Column

</td><td>

Field used as the source of the data for the columns in the heatmap. To select a source field on an extended table, see [How to report on extended tables.](../task/t_AccessFieldExtendedTable.md#) Select the info icon ![](../../par-for-workspace/image/icon-info.png) for a description of the selected field.

**Note:** Label names longer than 20 characters may show or print a truncated view.

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

Max number of groups

</td><td>

Maximum number of groups that the **Group by** condition returns. The groups with highest values are shown first. Any groups beyond the limit are combined into the single group **Other**.If you select **Show all**, all groups up to a limit of 50 are displayed. The rest of the results are grouped as **Other**.

</td></tr><tr><td>

Show Other

</td><td>

Check box to include the Other group in the report. The Other group contains data for all groups that exceed the number specified in **Max number of groups**.

</td></tr></tbody>
</table>6.  Configure the sort order of the applicable fields in the report \(column, row, Group by, Stack by or Trend by depending on the report type\).

    Select the filter icon \(![Filter icon for lists](../../../common/image/List_FilterIcon.png)\) and choose **Add Sort**.

    1.  In the Sorting Order list, choose the field you want to sort on and then choose **a-z** or **z-a** for alphabetical order or reverse alphabetical order.

        The list contains all possible fields from the report's source and fields on extended, or related, tables. The only effective values, however, are the fields chosen for the current report \(column, row, Group by, Stack by, or Trend by depending on the report type\).

        **Note:** On fields from dot-walked \(extended\) tables, you can only sort on date fields.

    2.  Select the sort plus icon \(![Sort plus icon](../image/sort-order-plus-icon.png)\) to configure additional sorting order conditions. \(Select the sort minus icon \( ![Sort minus icon](../image/sort-order-minus-icon.png)\) to delete configured sorting order conditions.\)
    3.  Select **Save**.
    For fields of the type Choice list, sort order is not determined alphabetically based on Label, it is sorted based on the **Value** of the choice field. For multi-level pivot table and heatmap reports, sort order is determined by the sequence of the choices in the list.

    ![Report sorted by priority choice list](../image/choice-list-sort-order.png)

7.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

8.  On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

## Heatmap report style options

Change the look of your heatmap chart.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

<table id="table_h5j_tx4_bs"><thead><tr><th class="sub-head" colspan="2">

General

</th></tr></thead><tbody><tr><td>

Use heatmap colors

</td><td>

Check box to use different colors to indicate different values.

</td></tr><tr><td>

Color for high scores

</td><td>

Color used to indicate a high value on the chart.

</td></tr><tr><td>

Color for low scores

</td><td>

Color used to indicate a low value on the chart.

</td></tr><tr><td>

Display data labels

</td><td>

Check box to show the value for each data point.

</td></tr><tr><td>

Display Zero

</td><td>

Select this check box to display the number **0** when the value of a cell is 0. Clear this check box to display an empty cell when the value of the cell is 0.

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

List view to show when a user selects a segment of a report for which no drilldown report type is specified. This view is also used when the user reaches the lowest drilldown level of a report. See [Configure the list layout](https://www.servicenow.com/docs/access?context=t_ConfigureTheListLayout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) . If you specify a **Report drilldown**, **Drilldown view** is ignored.For more information, see [Define a report drilldown](c_DrillingDownWithinReports.md#).

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

Legend

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
</table>