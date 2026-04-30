---
title: Dot walk fields in Visualization Designer
description: Learn how to dot walk table fields in a data visualization of table data. See how to start from a parent table, such as Task, and dot walk to include data from extended tables, such as Indicator and Problem.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [extended table]
breadcrumb: [Dot-walking from reference fields, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Dot walk fields in Visualization Designer

Learn how to dot walk table fields in a data visualization of table data. See how to start from a parent table, such as Task, and dot walk to include data from extended tables, such as Indicator and Problem.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin.

## About this task

**Note:** If you cannot dot-walk from any of your fields, check with a ServiceNow AI Platform administrator whether the system UI property **glide.ui.list.allow\_extended\_fields** is enabled on your instance.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Create any of the data visualizations listed under [Creating data visualizations](../concept/creating-data-visualizations.md), selecting a table data source.

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


## Dot-walking to two tables that extend Task \[task\]

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

**Parent Topic:**[Dot-walking from reference fields in a data visualization](ext-table-fields-dot-walk-vis-des.md)

