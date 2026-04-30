---
title: Box reports
description: Box reports, also called box plots, visualize the distribution of data including the maximum, minimum, quartiles, median, and mean.Create a box report to show the distribution of values in a data set.Configure the look of your box report.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2024-10-07"
reading_time_minutes: 12
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Box reports

Box reports, also called box plots, visualize the distribution of data including the maximum, minimum, quartiles, median, and mean.

Use box charts to report multiple data sets from different sources that are related to each other.

For example, use a box chart to view the age range of all customers who attended a convention. The box chart helps you determine where most ages are grouped. With this information, you can attempt to increase attendance levels at future events by targeting advertisements at the age groups that had lower attendance levels.

**Note:** This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see [Create a box plot data visualization](../task/create-dv-box-plot.md).

![Box report](../image/BoxChart.png "Box chart")

A box chart displays the following information for each group of data:

![1. Sample maximum: 2. Upper quartile 3. Median 4. Mean 5. Lower quartile 6. Sample minimum](../image/BoxChartScale.png "Box chart scale")

1.  Sample maximum
2.  Upper quartile
3.  Median
4.  Mean
5.  Lower quartile
6.  Sample minimum

**Note:** When accessibility is enabled, this visualization includes a report that screen readers can interpret. For more information, see [Enabling accessibility features](https://www.servicenow.com/docs/access?context=c_SetUpSect508ComplianceFeature&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Create a box report

Create a box report to show the distribution of values in a data set.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### About this task

Box reports enable you to show data organised by statistical averages.

### Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d118286e243">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d118286e262">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td id="d118286e281">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d118286e306">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select **Next**.

5.  On the **Type** tab, enter **Box** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

6.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_ctb_krs_jp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group by

</td><td>

Group report data using the values of this field. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. To group by fields on extended tables, see [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#). Select the info icon \(![](../image/icon-info.png)\) for a description of the selected field. Configured function fields appear in this list after you save the report.

 **Note:**

-   It is not possible to group or stack reports by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   Grouping or stacking by Variables or Questions fields is not supported for reports based on database views.
-   Label names longer than 20 characters may show or print a truncated view.


</td></tr><tr><td>

Additional group by

</td><td>

Extra fields to group the report by. When you select **Additional group by** fields or function fields, the report includes a control at the bottom that allows you to group the report by any one of the additional fields. To group by fields on extended tables as well, see [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#). Click the info icon \(![](../image/icon-info.png)\) for descriptions of the selected fields Configured function fields appear in this list after you save the report.

**Note:**

-   You can see choices in the **Additional group by** list that do not appear in the main **Group by** list. The report does not support grouping or stacking by the extra fields you see. Unlike the main **Group by** choices, the **Additional group by** fields are not filtered. If you select an unsupported field, it has no effect.
-   The limitations listed for the main **Group by** field also apply to the **Additional group by** field.
 For more information, see [Add an additional group by or stack by](../task/add-additional-group-by-stack-by.md).

</td></tr><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Measured by

</td><td>

Field to use as a measurement for the data. Date and time fields are not supported for box charts. Select the info icon \(![](../image/icon-info.png)\) for a description of the selected field.

</td></tr></tbody>
</table>7.  Configure the sort order of the applicable fields in the report \(column, row, Group by, Stack by or Trend by depending on the report type\).

    Select the filter icon \(![](../../../common/image/List_FilterIcon.png)\) and choose **Add Sort**.

    1.  In the Sorting Order list, choose the field you want to sort on and then choose **a-z** or **z-a** for alphabetical order or reverse alphabetical order.

        The list contains all possible fields from the report's source and fields on extended, or related, tables. The only effective values, however, are the fields chosen for the current report \(column, row, Group by, Stack by, or Trend by depending on the report type\).

        **Note:** On fields from dot-walked \(extended\) tables, you can only sort on date fields.

    2.  Select the sort plus icon \(![](../image/sort-order-plus-icon.png)\) to configure additional sorting order conditions. \(Select the sort minus icon \( ![](../image/sort-order-minus-icon.png)\) to delete configured sorting order conditions.\)
    3.  Select **Save**.
    For fields of the type Choice list, sort order is not determined alphabetically based on Label, it is sorted based on the **Value** of the choice field. For multi-level pivot table and heatmap reports, sort order is determined by the sequence of the choices in the list.

    ![Report sorted by priority choice list](../image/choice-list-sort-order.png)

8.  To limit the information displayed in the report, select the filter icon \(![](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

9.  On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

10. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


### What to do next

-   Select the Report info icon \(![](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

## Box report style options

Configure the look of your box report.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

<table id="table_h1l_1jh_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

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

Title horizontal alignment

</td><td>

How the chart title is aligned horizontally. This field is available when the **Custom chart title position** option is cleared.

</td></tr><tr><td>

Title vertical alignment

</td><td>

How the chart title is aligned vertically. This field appears when **Custom chart title position** is cleared.

</td></tr><tr><td>

Chart title X position

</td><td>

Number of pixels to adjust the chart title position right or left. By default the title appears at the center top of the chart. To move the chart title to the right, enter a positive value. To move the title to the left, enter a negative value.This field appears only when **Custom chart title position** is selected.

</td></tr><tr><td>

Chart title Y position

</td><td>

Number of pixels to adjust the chart title position up or down. By default the title appears at the center top of the chart. To move up the chart title, enter a positive value. To move the chart title down, enter a negative value.This field appears only when **Custom chart title position** is selected.

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

Depending on configured [Highcharts](https://api.highcharts.com/highcharts/yAxis.min) settings, the minimum value may be rounded up or down. If you require the settings that affect this changed, contact the administrator.

</td></tr><tr><td>

To

</td><td>

Specify a maximum Y-axis value to limit the amount of information in the report. If you select an aggregation field that is not of the type **Number**, the **From** and **To** fields are not available.**Note:**

Depending on configured [Highcharts](https://api.highcharts.com/highcharts/yAxis.min) settings, the minimum value may be rounded up or down. If you require the settings that affect this changed, contact the administrator.

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