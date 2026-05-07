---
title: Pivot tables
description: Pivot tables aggregate data from a table into columns and rows, which you define. They help you quickly investigate the source of the summarized data. Non-empty cells display tooltips to indicate how many records the cell represents. Click a non-empty cell to display a breakdown of those records.Create a pivot table to aggregate data from a table into columns and rows. Tooltips indicate what the values represent.Change the look of your pivot report.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Pivot tables

Pivot tables aggregate data from a table into columns and rows, which you define. They help you quickly investigate the source of the summarized data. Non-empty cells display tooltips to indicate how many records the cell represents. Click a non-empty cell to display a breakdown of those records.

You can configure a filter to refine the data further and select the aggregation values.

**Note:** While the pivot table report is still available, no enhancements are planned for this report and limitations are not being fixed. For new reports and older reports with problems, use the multilevel pivot table report. The multilevel pivot table is more stable, has more features than the pivot table, and is being continuously maintained. For more information, see [Multilevel pivot table](c_MultilevelPivotCharts.md#).

![pivot table example](../image/PivotTable.png "Pivot table")

**Parent Topic:**[Report types](../reference/report-types-creation-details-rd.md)

## Create a pivot table

Create a pivot table to aggregate data from a table into columns and rows. Tooltips indicate what the values represent.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### About this task

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d175951e223">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d175951e242">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td id="d175951e261">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d175951e286">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **Pivot** in the filter, select the Pivot report type from the **Other** section, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_b1w_sh4_bs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Row

</td><td>

Select one field for the chart rows. The chart displays data broken down by a combination of row and column values. To select a source field on extended table, see [How to report on extended tables.](../task/t_AccessFieldExtendedTable.md#) Select the info icon ![](../../par-for-workspace/image/icon-info.png) for a description of the selected field.

</td></tr><tr><td>

Column

</td><td>

Select one field for the chart columns. The chart displays data broken down by a combination of row and column values. To select a source field on an extended table, see [How to report on extended tables.](../task/t_AccessFieldExtendedTable.md#) Select the info icon ![](../../par-for-workspace/image/icon-info.png) for a description of the selected field.

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
-   Search the [Community](https://community.servicenow.com/community?id=community_search&forums=b5291a2ddbd897c068c1fb651f9619e2&q=pivot) site for more insight or help with pivot reports.

**Note:** While the Import Export property glide.pdf.max\_rows applies to row limits for pdf data exports in the platform product, for pivot reports exported to pdf from the Reporting product, it sets the maximum number of total cells \(both rows and columns\).

## Pivot report style options

Change the look of your pivot report.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

<table id="table_h1l_1jh_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Drilldown view

</td><td>

List view to show when a user selects a segment of a report for which no drilldown report type is specified. This view is also used when the user reaches the lowest drilldown level of a report. See [Configure the list layout](https://www.servicenow.com/docs/access?context=t_ConfigureTheListLayout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) . If you specify a **Report drilldown**, **Drilldown view** is ignored.For more information, see [Define a report drilldown](c_DrillingDownWithinReports.md#).

</td></tr></tbody>
</table>