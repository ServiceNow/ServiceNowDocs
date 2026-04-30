---
title: Dot-walking from reference fields in a data visualization
description: Dot-walking provides access to fields on extended, or related, tables, enabling you to create data visualizations on fields from those tables.Learn how to dot walk table fields in a data visualization of table data. See how to start from a parent table, such as Task, and dot walk to include data from extended tables, such as Indicator and Problem.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [related tables, extended tables, dot-walking, extended table]
breadcrumb: [Platform Analytics]
---

# Dot-walking from reference fields in a data visualization

Dot-walking provides access to fields on extended, or related, tables, enabling you to create data visualizations on fields from those tables.

You can access references on extended tables from the Metric, Group by/Stack by, column/row, or Trend by fields in the Configuration panel, or when you add custom conditions when you choose the data source. The Sorting option also enables you to configure the sort order of applicable reference fields on extended tables. Tables that reference other tables are denoted with an arrow \(![Expand icon for data visualizations](../../par-for-workspace/image/icon-dv-expand.png)\) icon.

Dot-walking references a field by building a chain of field names separated by dots \(periods\). For instance, **incident.assigned\_to.company** references the company of the user assigned to an incident. The recommended limit for chain length is three levels.

**Note:** Dot-walking applies only to visualizations of table data sources.

**Parent Topic:**[Platform Analytics](../../performance-analytics/concept/c_performanceAnalyticsAndReporting.md)

**Related topics**  


[Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

## Dot walk fields in Visualization Designer

Learn how to dot walk table fields in a data visualization of table data. See how to start from a parent table, such as Task, and dot walk to include data from extended tables, such as Indicator and Problem.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin.

### About this task

**Note:** If you cannot dot-walk from any of your fields, check with a ServiceNow AI Platform administrator whether the system UI property **glide.ui.list.allow\_extended\_fields** is enabled on your instance.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Create any of the data visualizations, selecting a table data source.

4.  Open one of the following sections of the configuration tab, depending on the visualization type:

    -   The condition builder that opens with **+ Add custom conditions** on the data source.
    -   Metric
    -   Group by
    -   Trend by
    -   Columns
5.  Edit or add an item in the section

    For a metric, select an aggregation other than Count.

6.  Under Field, navigate to the desired reference field.

    Reference fields have an Expand arrow ![Expand icon for data visualizations](../../par-for-workspace/image/icon-dv-expand.png).

7.  Select the Expand arrow to show a list of fields in the table that the reference field points to.

    ![Dot-walking to the Incident.Category field.](../image/dv-ext-tables-choose-field.png)

8.  Select a field, or continue to dot walk across reference fields until you find the desired field.

9.  Select **OK** or **Apply**.


### Dot-walking to two tables that extend Task \[task\]

In this example, you create a simple list of data from the Task table and include fields from the Indicator \[indicator\] and Problem \[problem\] tables, which extend Task.

1.  You navigate to the Data Visualizations list in the Platform Analytics library and select **New**.
2.  In the **Visualization type** field, you select Simple list \(![simple list icon](../image/inline-data-vis-list.png)\).
3.  In the Configuration tab, you keep the default Task \[task\] table.

    ![Report on extended tables in Visualization Designer, Configuration panel, with visualization name Active Incidents and Problems of Priority 1 or 2, Source type=Table, and Table=Task](../image/report-ext-tables-data-vis-des.png)

4.  In the Columns field, you select **+Add** and scroll down to Incident.
5.  Next to Incident, you see an Expand arrow ![Expand icon for data visualizations](../../par-for-workspace/image/icon-dv-expand.png) that indicates you can dot-walk. So you click that arrow, and scroll down through the fields on the Incident table until you reach the Category field, which you select.

    ![Dot-walking to the Incident.Category field.](../image/dv-ext-tables-choose-field.png)

6.  You repeat this process to add the Problem.Related incident field.
7.  Add the Number, State, Assigned to, and Short Description fields, and move them into the order you want.
8.  To see only relevant entries, you add the following filters:
    -   Active is true AND
    -   Category \[Incident\] is not Null OR
    -   Related Incidents \[Problem\] is not empty
9.  You save the visualization and title it `Active Incidents and Problems`.

The final visualization shows either Incident.Category values, Problem.Related Incidents values, or both.

![Data visualization showing Incident.Category data.](../image/dv-extended-table-category.png "Active Incidents and Problems data visualization showing Incident.Category content")

![Data visualization showing Problem.Related incident data.](../image/dv-extended-table-rel-incidents.png "Active Incidents and Problems data visualization showing Related incident.Problem content")

