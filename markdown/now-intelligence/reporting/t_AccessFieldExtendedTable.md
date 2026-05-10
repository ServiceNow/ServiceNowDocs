---
title: Report on extended tables
description: Learn how to include fields from tables that extend the Task table in a single report. For example, you could include both incidents and problems in a single report.Watch the video to learn how to use dot-walking, dynamic filters, and database views to access data on extended, or related, tables.Dot-walking provides access to fields on extended, or related, tables, enabling you to report on fields from those tables.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [related tables, extended tables, dot-walking]
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report on extended tables

Learn how to include fields from tables that extend the Task table in a single report. For example, you could include both incidents and problems in a single report.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

To include the columns in the report that are unique to the extended tables, a user with the admin role must enable a system property \[glide.ui.list.allow\_extended\_fields\]:

1.  Navigate to **System Properties** &gt; **UI Properties**.
2.  Enable the property **Allow base table lists \(task, cmdb\_ci, and so on\) to include extended table fields \(incident\_state, os\_version, and the like\), and allow filtering on extended table fields** \(glide.ui.list.allow\_extended\_fields\).
3.  Click **Save** at the bottom of the page.

## About this task

Watch this six-minute video to learn how to include fields on extended tables in reports by starting with the parent table.

How to include fields on extended tables, those not available through dot-walking

The video shows how to create a report with data from multiple tables using the Report Designer. The report contains both incidents and problems, which are child tables of the Task table. Here's how to create the report, Active Incidents and Problems of Priority 1 or 2.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  On the Data tab, name the report `Active Incidents and Problems of Priority 1 or 2`, select the Source type Table, and select the table Task \[task\].

    ![Report on extended tables in Report Designer, Data tab, with report name Active Incidents and Problems of Priority 1 or 2, Source type=Table, and Table=Task](../image/report-ext-tables-data.png)

3.  On the **Type** tab, enter **List** in the filter, select the report type, and click **Next**.

    The application shows a preliminary version of the report. To view the updated report at any time, select **Run**.

4.  On the **Configure** tab, Group by Task type and click **Save**.

    The list report is refreshed with all tasks collapsed into their types.![List report on the task table showing all task types.](../image/ext-table-list-rep-with-all-tasks.png)

5.  Click the filter icon \(![Filter icon](../image/icon-filter.png)\) to open the Condition Builder.

    Use the Condition Builder to limit what the report displays to only the information you want.

6.  To show only active incidents and problems of priority 1 or 2, set these conditions, and click **Save**.

    -   Active is true.
    -   Task type is Incident OR Task type is Problem.
    -   Priority is one of 1 - Critical or 2 - High.
    ![Condition builder showing the selected conditions Active, Task type, and priority conditions](../image/related-fields-task-conditions.png)

    The new report only has the two task types. Because you selected only Active tasks, there are fewer tasks in each category as well.

    ![List report on the Task table showing only active Incidents and Problems.](../image/ext-table-list-rep-with-tasks-filtered.png)

7.  Select the columns to display in the report, including the extended table fields Category \[Incident\] and Related Incidents \[Problem\] and click **Save**.

    ![Available Columns with several columns moved Selected.](../image/related-fields-columnns.png)

    The Category \[Incident\] and Related Incidents \[Problem\] fields are unique to the extended tables \(Incident and Problem\). They appear at the bottom of the list of columns that are available from the Task table. These two fields are available because you enabled the property **Allow base table lists to include extended table fields, and allow filtering on extended table fields** \(glide.ui.list.allow\_extended\_fields\).

    The report shows the open incidents and their categories and the open problems with the number of their related incidents.


**Parent Topic:**[Advanced Core UI reporting topics](../concept/c_AdvancedReporting.md)

## Related tables in reporting

Watch the video to learn how to use dot-walking, dynamic filters, and database views to access data on extended, or related, tables.

Watch this five-minute video to learn how to use dot walking to include data from extended or related tables in reports. The video also discusses using dynamic filters in reports and reporting on database views.How to use dot-walking and database views to include data from extended, or related, tables in reports.

## Reporting on extended table fields using dot-walking

Dot-walking provides access to fields on extended, or related, tables, enabling you to report on fields from those tables.

When creating or editing a report, you can access references on extended tables from the Group by/Stack by, column/row, or Trend by fields on the Configure tab. The Add Sort option also enables you to configure the sort order of applicable reference fields on extended tables. Tables that reference other tables are denoted with an arrow \(![](../image/extendedTableArrow.png)\) icon.

Dot-walking references a field by building a chain of field names separated by dots \(periods\). For example, **incident.assigned\_to.company** references the company of the user assigned to an incident. The recommended limit for chain length is three levels.

1.  In a report on the incident table, select **Additional Group By** on the Configure tab.
2.  Select Assigned to \[+\] and then the structure icon \(![](../image/Form_ShowReportStructureIcon.png)\).

    You now see the related fields in the user table.

3.  Move Company \[+\] to the **Selected** column and select **OK**.
4.  Save the report.

    Assigned to Company is an option in the report's Group by list. In this example, you see Assigned to Active because the Active field is a configured Stack by option.

    ![Report on extended tables with Assigned to Company option selected in Group by](../image/report-ext-table-result.png)


**Related topics**  


[Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md)

