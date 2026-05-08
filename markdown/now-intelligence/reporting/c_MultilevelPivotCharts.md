---
title: Multilevel pivot tables
description: Multilevel pivot tables display aggregate data broken down by multiple dimensions in a single table. They display separate cells for each row and column value combination, as well as a column subtotal for each first-level row. Aggregate information is presented in the top left of the chart.Create a multilevel pivot report to display aggregate data broken down by multiple metrics in a single table.You can create a multilevel pivot report with variables columns and rows based on a data source or table that has variables associated with it. Variables are descriptions of catalog items.Change the look of your multi-level pivot chart.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Multilevel pivot tables

Multilevel pivot tables display aggregate data broken down by multiple dimensions in a single table. They display separate cells for each row and column value combination, as well as a column subtotal for each first-level row. Aggregate information is presented in the top left of the chart.

You can also create multilevel pivot tables with columns and rows containing variables. See [Use service catalog variables in a report](../task/use-service-catalog-variables-in-report.md).

You can expand and collapse the rows in the table to show the chart details, or only the subtotals. The top row of a multilevel pivot report is always visible.

**Note:**

-   On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).
-   Some row configurations prevent the chart from displaying subtotal information, such as when a string column has the same text value but with different character cases.
-   You can only schedule this report type as a PDF.

![A multilevel pivot table with subtotals and expanded rows](../image/multilevel-pivot-report-example.png "Multilevel pivot with subtotals and expanded rows")

**Parent Topic:**[Report types](../reference/report-types-creation-details-rd.md)

## Create a multilevel pivot report

Create a multilevel pivot report to display aggregate data broken down by multiple metrics in a single table.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

**Note:** On net new Australia instances, only users with the report\_admin role can create reports. To visualization your information in these instances, see [Creating data visualizations](creating-data-visualizations.md).

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d204483e288">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d204483e307">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see Retrieving external data using remote tables and scripts

</td></tr><tr><td id="d204483e326">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d204483e351">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see MetricBase.

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **Multi-level pivot table** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_b1w_sh4_bs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select columns

</td><td>

One or more fields to use as chart columns. The chart displays data broken down by a combination of row and column values. You can select up to three columns. Select the info icon ![](../../par-for-workspace/image/icon-info.png) for descriptions of the selected fields

**Note:** It is not possible to group by the **Tags** field.

</td></tr><tr><td>

Select rows

</td><td>

One or more fields to use as chart rows. The chart displays data broken down by a combination of row and column values. You can select up to five rows. Select the info icon ![](../../par-for-workspace/image/icon-info.png) for descriptions of the selected fields

**Note:** The **Tags** field is not supported for multilevel pivot reports.

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

Set Value Formatting

</td><td>

Enables you to configure how to show numerical values in reports, including decimal precision, rounding, minimum and maximum duration units, and abbreviations for duration units. See [Value formatting in reports](../reference/value-formatting-reports.md#).

 **Note:** Decimal precision does not work on currency fields.

</td></tr><tr><td>

Max number of groups

</td><td>

Maximum number of groups that the **Group by** condition returns. The groups with highest values are shown first. Any groups beyond the limit are combined into the single group **Other**.If you select **Show all**, all groups up to a limit of 50 are displayed. The rest of the results are grouped as **Other**.

</td></tr><tr><td>

Show Other

</td><td>

Check box to include the Other group in the report. The Other group contains data for all groups that exceed the number specified in **Max number of groups**.

</td></tr></tbody>
</table>    **Note:** Currency fields default to two decimal places. With the **Set Value Formatting** option, you can configure decimal precision for 0-4 decimal places.

8.  Select **Default expanded** to display the report with the rows expanded.

    Otherwise, the report will display with all rows collapsed.

    ![Multilevel pivot report with collapsed and expanded rows](../image/multilevel-pivot-report-collapsed-rows.png "Multilevel pivot report with collapsed and expanded rows")

9.  Check **Display row lines** and **Display column lines** to show the lines that separate the cells in the report.

    ![Multilevel pivot report with row and column lines](../image/multilevel-pivot-with-row-column-lines.png)

10. Configure the sort order of the applicable fields in the report \(column, row, Group by, Stack by or Trend by depending on the report type\).

    Select the filter icon \(![Filter icon for lists](../../../common/image/List_FilterIcon.png)\) and choose **Add Sort**.

    1.  In the Sorting Order list, choose the field you want to sort on and then choose **a-z** or **z-a** for alphabetical order or reverse alphabetical order.

        The list contains all possible fields from the report's source and fields on extended, or related, tables. The only effective values, however, are the fields chosen for the current report \(column, row, Group by, Stack by, or Trend by depending on the report type\).

        **Note:** On fields from dot-walked \(extended\) tables, you can only sort on date fields.

    2.  Select the sort plus icon \(![Sort plus icon](../image/sort-order-plus-icon.png)\) to configure additional sorting order conditions. \(Select the sort minus icon \( ![Sort minus icon](../image/sort-order-minus-icon.png)\) to delete configured sorting order conditions.\)
    3.  Select **Save**.
    For fields of the type Choice list, sort order is not determined alphabetically based on Label, it is sorted based on the **Value** of the choice field. For multi-level pivot table and heatmap reports, sort order is determined by the sequence of the choices in the list.

    ![Report sorted by priority choice list](../image/choice-list-sort-order.png)

11. To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see Condition builder.

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

12. On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

13. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.
-   Search the [Community](https://community.servicenow.com/community?id=community_search&forums=b5291a2ddbd897c068c1fb651f9619e2&q=multilevel) site for more insight or help with multi-level pivot reports.

## Create a multilevel pivot report with variable columns and rows

You can create a multilevel pivot report with variables columns and rows based on a data source or table that has variables associated with it. Variables are descriptions of catalog items.

### Before you begin

Roles required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d204483e967">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d204483e986">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see Retrieving external data using remote tables and scripts

</td></tr><tr><td id="d204483e1005">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](../task/create-report-with-imported-data-source.md).

</td></tr><tr><td id="d204483e1030">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see MetricBase.

</td></tr></tbody>
</table>4.  Select **Next**.

5.  On the **Type** tab, enter **Multi-level pivot table** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

6.  On the **Configure** tab, click **Select columns**.

    From the Available list in the **Multilevel Pivot Columns** window, select columns that you want to use in the report and move them to the **Selected** list.

    **Note:** It is not possible to group or stack reports by the **Tags** field, or by certain field types, such as MEDIUMTEXT.

    Depending on system configuration, you can add fields from tables that extend the table selected as the report data source. For more information, see [Report on extended tables](../task/t_AccessFieldExtendedTable.md#).

7.  Select variables to use as columns:

    1.  Select one or more fields to use as report columns.

        The report visualization displays data broken down by a combination of row and column values. You can select up to three columns including the variables.

    2.  Select **Variables \[+\]** and click the structure icon \(![](../image/Form_ShowReportStructureIcon.png)\) to choose an item.

        ![Columns slushbucket](../image/columns-variables.png)

    3.  Select a **Catalog item** from the pop-up window.

        The variables associated with the item appear in the **Columns** window.

        ![Columns with selected item and variables](../image/columns-variables-selected.png)

    4.  Move the selected variables to the **Selected** column and click **OK**. Select the info icon ![](../../par-for-workspace/image/icon-info.png) for descriptions of the selected fields

8.  Click **Select rows** to select one or more fields to use as report rows.

    You select rows similarly to how you select columns. Select the info icon ![](../../par-for-workspace/image/icon-info.png) for descriptions of the selected fields.

    The report visualization displays data broken down by a combination of row and column values. You can select up to five rows including the variables.

    **Note:** It is not possible to group or stack reports by the **Tags** field, or by certain field types, such as MEDIUMTEXT.

9.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_b1w_sh4_bs"><thead><tr><th>

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

Mathematical calculation to perform on the data. The default is **Count**, which shows the number of records selected.To show only unique records, select **Count Distinct**.

 Select **Average**, **Sum**, or **Count Distinct**, to show a list of fields from the selected **Table**. Select a field to **Aggregate by** from this list.

 If you group the report by a field and select an **Average** aggregate, you get the average of each group. If a Total value is shown, it is the average of these group averages, not of the individual field values.

 Select **Minimum** or **Maximum** to show the maximum or minimum value for each segment of the report.

 For more information on aggregation options, see [Aggregation in reporting](../reference/aggregation-reporting.md).

 If you choose **Average**,**Sum**, **Count Distinct**, **Minimum**, or **Maximum**, you may be able to aggregate on fields from extended tables. See [How to report on extended tables](../task/t_AccessFieldExtendedTable.md#).

 For information about aggregating on FX currency values, see [FX Currency values in reporting](fx-currency-values-reporting.md#).

</td></tr><tr><td>

Set Value Formatting

</td><td>

Enables you to configure how to show numerical values in reports, including decimal precision, rounding, minimum and maximum duration units, and abbreviations for duration units. See [Value formatting in reports](../reference/value-formatting-reports.md#).

 **Note:** Decimal precision does not work on currency fields.

</td></tr><tr><td>

Max number of groups

</td><td>

Maximum number of groups that the **Group by** condition returns. The groups with highest values are shown first. Any groups beyond the limit are combined into the single group **Other**.If you select **Show all**, all groups up to a limit of 50 are displayed. The rest of the results are grouped as **Other**.

</td></tr><tr><td>

Show Other

</td><td>

Check box to include the Other group in the report. The Other group contains data for all groups that exceed the number specified in **Max number of groups**.

</td></tr></tbody>
</table>    **Note:** Currency fields default to two decimal places. With the **Set Value Formatting** option, you can configure decimal precision for 0-4 decimal places.

10. Check **Display row lines** and **Display column lines** to show the lines that separate the cells in the report.

    ![Multilevel pivot report with row and column lines](../image/multilevel-pivot-with-row-column-lines.png)

11. Configure the sort order of the applicable fields in the report \(column, row, Group by, Stack by or Trend by depending on the report type\).

    Select the filter icon \(![Filter icon for lists](../../../common/image/List_FilterIcon.png)\) and choose **Add Sort**.

    1.  In the Sorting Order list, choose the field you want to sort on and then choose **a-z** or **z-a** for alphabetical order or reverse alphabetical order.

        The list contains all possible fields from the report's source and fields on extended, or related, tables. The only effective values, however, are the fields chosen for the current report \(column, row, Group by, Stack by, or Trend by depending on the report type\).

        **Note:** On fields from dot-walked \(extended\) tables, you can only sort on date fields.

    2.  Select the sort plus icon \(![Sort plus icon](../image/sort-order-plus-icon.png)\) to configure additional sorting order conditions. \(Select the sort minus icon \( ![Sort minus icon](../image/sort-order-minus-icon.png)\) to delete configured sorting order conditions.\)
    3.  Select **Save**.
    For fields of the type Choice list, sort order is not determined alphabetically based on Label, it is sorted based on the **Value** of the choice field. For multi-level pivot table and heatmap reports, sort order is determined by the sequence of the choices in the list.

    ![Report sorted by priority choice list](../image/choice-list-sort-order.png)

12. To limit the information displayed in the report, select the filter icon \(![Filter icon](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see Condition builder.

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

13. On the **Style** tab, fill in the fields as appropriate to configure the appearance of the report.

14. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


### What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Select the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules.
-   Search the [Community](https://community.servicenow.com/community?id=community_search&forums=b5291a2ddbd897c068c1fb651f9619e2&q=multilevel) site for more insight or help with multi-level pivot reports.

## Multilevel pivot report style options

Change the look of your multi-level pivot chart.

When you create or edit a report, click the **Style** tab for options to configure the look of your report. The options are organized under two or more of the following tabs: **General**, **Title**, **Legend**, and **Axis**. To see how the report looks with the changed settings, click **Save**.

<table id="table_h1l_1jh_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Display Zero

</td><td>

Check this box to display the number **0** when the value of a cell is 0. Clear this check box to display an empty cell when the value of the cell is 0. Applicable when **Aggregation** is **Count** or **Count Distinct**.

</td></tr><tr><td>

Default expanded

</td><td>

Check this box to expand all rows when the report is displayed. Clear this check book to collapse all rows when the report is displayed. ![Multilevel pivot report with collapsed and expanded rows](../image/multilevel-pivot-report-collapsed-rows.png)

</td></tr><tr><td>

Display row lines

</td><td>

Check this box to display lines between rows in the report.

</td></tr><tr><td>

Display column lines

</td><td>

Check this box to display lines between columns in the report.

</td></tr><tr><td>

Drilldown view

</td><td>

List view to show when a user selects a segment of a report for which no drilldown report type is specified. This view is also used when the user reaches the lowest drilldown level of a report. See Configure the list layout . If you specify a **Report drilldown**, **Drilldown view** is ignored.For more information, see [Define a report drilldown](c_DrillingDownWithinReports.md#).

</td></tr><tr id="EditColoringRules"><td>

Edit coloring rules

</td><td>

Click this hyperlink to configure how cells and cell text with numerical values are colored in the report. You can create rules to define which colors are used based on operators and values. For example, you can specify that any value greater than 5 displays in red. See [Create coloring rules for multilevel pivot reports](../task/t_DefineAPivotTableColoringRule.md).**Note:** It is not possible to apply coloring rules to the Total cells in multilevel pivot reports.

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

Title horizontal alignment

</td><td>

How the chart title is aligned horizontally. This field is available when the **Custom chart title position** option is cleared.

</td></tr><tr><td>

Title vertical alignment

</td><td>

How the chart title is aligned vertically. This field appears when **Custom chart title position** is cleared.

</td></tr></tbody>
</table>