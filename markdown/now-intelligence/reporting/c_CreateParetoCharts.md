---
title: Pareto reports
description: Pareto charts help you identify the most important dimension in a large set of dimensions. Columns show data in descending order. A line shows cumulative percentage.Create a Pareto report to identify the most important factors in a large set of factors. Columns show data in descending order while a curve shows cumulative percentage.Change the look of your Pareto report.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Pareto reports

Pareto charts help you identify the most important dimension in a large set of dimensions. Columns show data in descending order. A line shows cumulative percentage.

Pareto charts contain both bar and line graphs. The bars display the data in descending order from left to right, and the line graph shows the cumulative totals from each category in the same order. The left Y axis is the record count, and the right Y axis is the cumulative percentage of the total number of records evaluated. The blue line at the 80% mark helps determine which data is the most influential in the process. The data to the left of the intersection of the line graph and the 80% mark have the greatest effect on the overall outcome.

**Note:** On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).

The figure below shows that five callers account for 80% of the incident calls, while seven account for the other 20%.

![Pareto chart](../image/pareto-report-instance-by-caller.png "Pareto report example")

**Parent Topic:**[Report types](../reference/report-types-creation-details-rd.md)

## Create a Pareto report

Create a Pareto report to identify the most important factors in a large set of factors. Columns show data in descending order while a curve shows cumulative percentage.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d136687e266">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d136687e285">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td id="d136687e304">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d136687e329">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **Pareto** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_pvl_jx1_rq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group by

</td><td>

Group report data using the values of this field. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. To group by fields on extended tables, see [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#). Select the info icon ![](../../par-for-workspace/image/icon-info.png) for a description of the selected field. Configured function fields appear in this list after you save the report.

 **Note:**

-   It is not possible to group or stack reports by the **Tags** field, or by certain MySQL database field types, such as MEDIUMTEXT. For more information, see [Database field type](https://www.servicenow.com/docs/access?context=r_DatabaseFieldTypes&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Grouping or stacking by Variables or Questions fields is not supported for reports based on [database views](../../performance-analytics/concept/performance-analytics-glossary.md#).


</td></tr><tr><td>

Additional group by

</td><td>

Extra fields to group the report by. When you select **Additional group by** fields or function fields, the report includes a control at the bottom that allows you to group the report by any one of the additional fields. To group by fields on extended tables as well, see [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#). Select the info icon ![](../../par-for-workspace/image/icon-info.png) for descriptions of the selected fields Configured function fields appear in this list after you save the report.

**Note:**

-   You can see choices in the **Additional group by** list that do not appear in the main **Group by** list. The report does not support grouping or stacking by the extra fields you see. Unlike the main **Group by** choices, the **Additional group by** fields are not filtered. If you select an unsupported field, it has no effect.
-   The limitations listed for the main **Group by** field also apply to the **Additional group by** field.
 For more information, see [Add an additional group by or stack by](../task/add-additional-group-by-stack-by.md).

</td></tr><tr><td>

Display data table

</td><td>

Select this option to show report data in a list below the report. The list appears on dashboards where the report is added.All report visualizations show the report data when the [glide.ui.section508](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US) system property is set to **true**. The glide.ui.section508 property overrides the **Display data table** field.

</td></tr><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr><tr><td>

Max number of groups

</td><td>

Maximum number of groups that the **Group by** condition returns. The groups with highest values are shown first. Any groups beyond the limit are combined into the single group **Other**.If you select **Show all**, all groups up to a limit of 50 are displayed. The rest of the results are grouped as **Other**.

</td></tr><tr><td>

Show Other

</td><td>

Check box to include the Other group in the report. The Other group contains data for all groups that exceed the number specified in **Max number of groups**.

</td></tr></tbody>
</table>8.  Configure the sort order of the applicable fields in the report \(column, row, Group by, Stack by or Trend by depending on the report type\).

    Select the filter icon \(![Filter icon for lists](../../../common/image/List_FilterIcon.png)\) and choose **Add Sort**.

    1.  In the Sorting Order list, choose the field you want to sort on and then choose **a-z** or **z-a** for alphabetical order or reverse alphabetical order.

        The list contains all possible fields from the report's source and fields on extended, or related, tables. The only effective values, however, are the fields chosen for the current report \(column, row, Group by, Stack by, or Trend by depending on the report type\).

        **Note:** On fields from dot-walked \(extended\) tables, you can only sort on date fields.

    2.  Select the sort plus icon \(![Sort plus icon](../image/sort-order-plus-icon.png)\) to configure additional sorting order conditions. \(Select the sort minus icon \( ![Sort minus icon](../image/sort-order-minus-icon.png)\) to delete configured sorting order conditions.\)
    3.  Select **Save**.
    For fields of the type Choice list, sort order is not determined alphabetically based on Label, it is sorted based on the **Value** of the choice field. For multi-level pivot table and heatmap reports, sort order is determined by the sequence of the choices in the list.

    ![Report sorted by priority choice list](../image/choice-list-sort-order.png)

9.  To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

10. On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

11. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.

## Pareto report style options

Change the look of your Pareto report.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

**Note:** The cumulative totals percentage line is not configurable. It cannot be disabled and the color cannot be changed.

<table id="table_h1l_1jh_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Chart color

</td><td>

Source of colors used in the report. If you are not stacking the report by a field, you can select one of the following options:-   **Use one color**: Select a single predefined color in the **Chart color field**.
-   **Use color palette**: Select a color palette from the predefined system color palettes.
-   **Use chart colors**: Use the colors defined in **Reports** &gt; **Chart Colors**.

 If you are stacking the report, select one of the following options:

-   **Use color palette**: Select a color palette from the predefined system color palettes.
-   **Use several colors**: Define a custom set of **Colors** using hex codes. You can add any number of colors.
-   **Use chart colors**: Use the colors defined in **Reports** &gt; **Chart Colors**.

 For more information about the differences between these options, see [Predefined colors in reports](colors-reports.md).

</td></tr><tr><td>

Set color

</td><td>

Color used in the report. This field displays when you select **Use one color** from the **Chart color** list. Click the search icon \(![Search icon](../image/SearchIcon.png)\) to choose from the **Color Definitions** list.

</td></tr><tr><td>

Set palette

</td><td>

Color palette used in the report. This field appears when you select **Use color palette** from the **Chart color** list. The palettes are defined in the Chart Color Scheme \[pa\_chart\_color\_schemes\] table.

</td></tr><tr><td>

Colors

</td><td>

Colors used in the report. This field displays when you select **Use several colors** from the **Chart color** list. Enter a comma-separated list of hexadecimal color codes. These colors are independent of the predefined system colors that color palettes and the chart colors use.**Note:** It is not possible to use transparency hex values.

</td></tr><tr><td>

Display data labels

</td><td>

Select to display the current value for each bar. This field is available when you select None from the **Stacked by** list or if there is no **Stacked by** list.-   Select **Data labels in the middle** to show the labels in the middle of each bar.
-   Select **Allow data labels to overlap** to override default separation of labels in the visualization.

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

Enable this option to show the axis title in a bold typeface.

</td></tr><tr><td>

Title bold

</td><td>

Enable this option to show the axis title in a bold typeface.

</td></tr><tr><td>

Opposite

</td><td>

On the **X axis** tab, enable this option to show the X-axis title on the right side of the report instead. On the **Y axis** tab, enable this option to show the Y-axis title on top of the report instead of across the bottom.

</td></tr><tr><td>

Display grid

</td><td>

On the **X axis** tab, enable this option to show horizontal grid lines on the report. On the **Y axis** tab, enable this option to show vertical grid lines on top the report.

</td></tr><tr><td>

Grid dotted

</td><td>

Enable this option to show dotted grid lines instead of solid lines.

</td></tr><tr><td>

X axis / Y axis label size

</td><td>

On the **X axis** tab, specify the size of the labels for the rows of the report. On the **Y axis** tab, specify the size of the labels for the columns in the report.

</td></tr><tr><td>

Label bold

</td><td>

Enable this option to show the labels of the report in a bold typeface.

</td></tr></tbody>
</table>