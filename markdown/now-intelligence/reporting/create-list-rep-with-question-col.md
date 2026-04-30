---
title: Create a list report with question columns
description: You can create a list report with question columns based on a data source or table that has questions associated with it. For example, if a form prompts a user to select the specific nature of a problem, you can create a list report that lists columns for those values.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [List reports, Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a list report with question columns

You can create a list report with question columns based on a data source or table that has questions associated with it. For example, if a form prompts a user to select the specific nature of a problem, you can create a list report that lists columns for those values.

## Before you begin

Roles required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select a report source that has variables associated with it.

    There are two kinds of report sources. For list reports with variables, the report source is usually the service catalog table.

<table id="simpletable_wrg_yz2_4wb"><thead><tr><th>

Report source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

A table with filters applied to provide a single source of information for all users. **Note:** If you select a data source used by existing reports, a notification will display prompting you to view them.

</td></tr><tr><td>

Table

</td><td>

The raw data from a table with no filters applied.

</td></tr></tbody>
</table>4.  Select **Next**.

5.  On the **Type** tab, enter **List** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

6.  On the **Configure** tab, click **Choose columns** and select **Questions \[+\]** in the Columns window that opens.

    **Questions \[+\]** is at the bottom of the list of available columns.

    Depending on system configuration, you can add fields from tables that extend the selected table. For more information, see [Report on extended tables](t_AccessFieldExtendedTable.md#).

7.  Click the structure icon \(![](../image/Form_ShowReportStructureIcon.png)\) to choose an item.

    ![Columns slushbucket](../image/columns-questions.png)

8.  Select an item from the Catalog item list that appears.

    The variables associated with the selected item then appear in the **Columns** window.

    ![Columns with selected item and questions](../image/columns-questions-selected.png)

9.  Select and move questions to the **Selected** column and click **OK**.

10. On the **Configure** tab, fill in the following fields and select **Next**.

<table id="table_wvg_5jr_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group by

</td><td>

Group report data using the values of this field. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. To group by fields on extended tables, see [How to report on extended tables](t_AccessFieldExtendedTable.md#). Select the info icon \(![](../image/icon-info.png)\) for a description of the selected field. Configured function fields appear in this list after you save the report.

 **Note:**

-   It is not possible to group or stack reports by the **Tags** field, or by certain MySQL database field types, such as MEDIUMTEXT. For more information, see [Database field type](https://www.servicenow.com/docs/access?context=r_DatabaseFieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Grouping or stacking by Variables or Questions fields is not supported for reports based on [database views](../../performance-analytics/concept/performance-analytics-glossary.md#).


</td></tr><tr><td>

Additional group by

</td><td>

Extra fields to group the report by. When you select **Additional group by** fields or function fields, the report includes a control at the bottom that allows you to group the report by any one of the additional fields. To group by fields on extended tables as well, see [How to report on extended tables](t_AccessFieldExtendedTable.md#). Click the info icon \(![](../image/icon-info.png)\) for descriptions of the selected fields Configured function fields appear in this list after you save the report.

**Note:**

-   You can see choices in the **Additional group by** list that do not appear in the main **Group by** list. The report does not support grouping or stacking by the extra fields you see. Unlike the main **Group by** choices, the **Additional group by** fields are not filtered. If you select an unsupported field, it has no effect.
-   The limitations listed for the main **Group by** field also apply to the **Additional group by** field.
 For more information, see [Add an additional group by or stack by](add-additional-group-by-stack-by.md).

</td></tr><tr><td>

Configure function field

</td><td>

Configure fields based on calculation of multiple inputs including arithmetic functions. For more information, see [Report on function fields](../concept/function-fields-reporting.md). Function field results are calculated when the report is run. You can use the results for aggregations and grouping. You have to save the report before you can configure function fields.Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

</td></tr></tbody>
</table>11. Configure the sort order of the applicable fields in the report \(column, row, Group by, Stack by or Trend by depending on the report type\).

    Select the filter icon \(![](../../../common/image/List_FilterIcon.png)\) and choose **Add Sort**.

    1.  In the Sorting Order list, choose the field you want to sort on and then choose **a-z** or **z-a** for alphabetical order or reverse alphabetical order.

        The list contains all possible fields from the report's source and fields on extended, or related, tables. The only effective values, however, are the fields chosen for the current report \(column, row, Group by, Stack by, or Trend by depending on the report type\).

        **Note:** On fields from dot-walked \(extended\) tables, you can only sort on date fields.

    2.  Select the sort plus icon \(![](../image/sort-order-plus-icon.png)\) to configure additional sorting order conditions. \(Select the sort minus icon \( ![](../image/sort-order-minus-icon.png)\) to delete configured sorting order conditions.\)
    3.  Select **Save**.
    For fields of the type Choice list, sort order is not determined alphabetically based on Label, it is sorted based on the **Value** of the choice field. For multi-level pivot table and heatmap reports, sort order is determined by the sequence of the choices in the list.

    ![Report sorted by priority choice list](../image/choice-list-sort-order.png)

12. To limit the information displayed in the report, select the filter icon \(![](../../../common/image/List_FilterIcon.png)\) and specify conditions to filter the report data.

    To learn how to construct conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    **Note:** In aggregated and list reports, language-dependent filter conditions may return zero results on localized instances.

13. On the **Style** tab, add and configure a report title.

    See [List report style options](../reference/list-report-style-options.md).

14. Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


## What to do next

-   Select the Report info icon \(![](../../../common/image/Form_ReferenceLookupIcon.png)\) and add a description of the report.
-   Click the sharing icon \(![](../image/ShareIcon.png)\) to open the **Sharing** menu. On this menu, you can add the report to a dashboard, export the report to PDF, publish the report to the web, and set visibility and schedules. For more information, see [Share a report](t_ShareASetting.md).

    **Note:** The default number of rows in a list report exported to PDF is 1000. To configure this value, enter `sys_properties.list` in the Filter Navigator, and edit the property glide.pdf.max\_rows. For more information, see: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).


