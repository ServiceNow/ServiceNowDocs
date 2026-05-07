---
title: Create a basic list report
description: List reports display data in the form of an expandable list. For example, an incident report grouped by priority displays only the priority names and a number of records that display if the user clicks the priority. You can configure whether lists display expanded or collapsed.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [List reports, Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a basic list report

List reports display data in the form of an expandable list. For example, an incident report grouped by priority displays only the priority names and a number of records that display if the user clicks the priority. You can configure whether lists display expanded or collapsed.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

3.  On the **Data** tab, give the report a name that reflects the information being grouped.

4.  Select the applicable source for the report.

<table id="choicetable_t31_tst_1x"><tbody><tr><td id="d163454e141">

**Data source**

</td><td>

Also called a report source, a data source is a table with filters applied to provide a single source of information for all users. For more information, see [Report sources](../concept/c_ReportSources.md#).**Note:** If you select a data source used by existing reports, a notification prompts you to view them.

</td></tr><tr><td id="d163454e160">

**Table**

</td><td>

The raw data from a table with no filters applied. When you select a table, its short description appears below the table name. For trend reporting, you can also select a remote table, which aggregates, in memory, data retrieved from an external source. Then select a **Trend by** field option to aggregate its data. To learn more about remote tables, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td id="d163454e179">

**External import**

</td><td>

Choose an existing imported report source, or select the Upload icon \(![Upload icon](../image/upload-icon.png)\) to import a new file. See [Create a Core UI report from an imported Microsoft Excel document](create-report-with-imported-data-source.md).

</td></tr><tr><td id="d163454e204">

**MetricBase**

</td><td>

MetricBase enables you to collect, retain, analyze, and visualize custom time series data on the ServiceNow AI Platform. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Select **Next**.

6.  On the **Type** tab, enter **List** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

7.  On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_wvg_5jr_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choose columns

</td><td>

Fields to display as columns in the list report. In the Columns window that opens after you click **Choose columns**, select fields in the Available list that you want to appear in your report and move them to the Selected list. Select the info icon ![](../../par-for-workspace/image/icon-info.png) for descriptions of the selected fields

 Depending on system configuration, you can add fields from tables that extend the selected table. For more information, see [Report on extended tables](t_AccessFieldExtendedTable.md#).

</td></tr><tr><td>

Group by

</td><td>

Group report data using the values of this field. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. To group by fields on extended tables, see [How to report on extended tables](t_AccessFieldExtendedTable.md#). Select the info icon ![](../../par-for-workspace/image/icon-info.png) for a description of the selected field. Configured function fields appear in this list after you save the report.

 **Note:**

-   It is not possible to group or stack reports by the **Tags** field, or by certain MySQL database field types, such as MEDIUMTEXT. For more information, see [Database field type](https://www.servicenow.com/docs/access?context=r_DatabaseFieldTypes&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Grouping or stacking by Variables or Questions fields is not supported for reports based on [database views](../../performance-analytics/concept/performance-analytics-glossary.md#).


</td></tr><tr><td>

Additional group by

</td><td>

Extra fields to group the report by. When you select **Additional group by** fields or function fields, the report includes a control at the bottom that allows you to group the report by any one of the additional fields. To group by fields on extended tables as well, see [How to report on extended tables](t_AccessFieldExtendedTable.md#). Select the info icon ![](../../par-for-workspace/image/icon-info.png) for descriptions of the selected fields Configured function fields appear in this list after you save the report.

**Note:**

-   You can see choices in the **Additional group by** list that do not appear in the main **Group by** list. The report does not support grouping or stacking by the extra fields you see. Unlike the main **Group by** choices, the **Additional group by** fields are not filtered. If you select an unsupported field, it has no effect.
-   The limitations listed for the main **Group by** field also apply to the **Additional group by** field.
 For more information, see [Add an additional group by or stack by](add-additional-group-by-stack-by.md).

</td></tr><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](../concept/function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

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

10. On the **Style** tab, add and configure a report title.

    See [List report style options](../reference/list-report-style-options.md).

11. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


## What to do next

-   Select the Report info icon \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Click the sharing icon \(![Sharing icon](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules. For more information, see [Share a Core UI report](t_ShareASetting.md).

    **Note:**

    -   The default number of rows in a list report exported to PDF is 1000. To configure this value, enter `sys_properties.list` in the Filter Navigator, and edit the property glide.pdf.max\_rows. For more information, see: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).
    -   Despite list filtering, pdf-format exported rows will count all record rows sequentially up to the export limit and show as blank for roles prevented by ACLs from viewing restricted data.
-   [Configure and use list functions](https://www.servicenow.com/docs/access?context=configure-use-list-functions&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

**Parent Topic:**[List reports](../concept/list-reports.md)

