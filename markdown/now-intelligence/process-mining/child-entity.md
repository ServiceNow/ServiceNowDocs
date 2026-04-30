---
title: Add a child entity
description: Add a child or related table to track an activity from a related process.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Add a child entity

Add a child or related table to track an activity from a related process.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## About this task

Often the start and end of a full workflow occurs outside the life cycle of your business process. When it's helpful to analyze these external events, you can add another table for tracking other events relevant to your process. For example, if Incident table is your parent table, and you define the Incident Task \[incident\_task\] table as child table for the Incident table, then when a record from the Incident Task \[incident\_task\] table is created, it shows as an 'Incident Task created' activity on the process map. Only 'created' or 'closed' events show as activities in the process graph.

**Note:** External events from a defined child table don’t show as condition options in the Transitions or condition filters.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Set Objectives** page, you are on the **Scope your analysis** page.

2.  Select **Edit** for the project you want to edit.

3.  Select the edit button for the **Scope your analysis** section.

4.  Select **Add child entity** from the left bar.

    **Tip:** Select **Advanced view** on the top right corner if you want to edit the project in the Classic view.

    ![](../image/child-entity.png)

5.  Fill in the form with the details.

<table id="table_cdk_gnq_vkb"><tbody><tr><td>

Source

</td><td>

The source for the table configuration. You can select a source type:-   Table: Any database table
-   Report source: A table that has reports
-   Archived data: An archived table


</td></tr><tr><td>

Select

</td><td>

Select a table that has a relationship with the parent table of your project.

</td></tr><tr><td>

Parent Table

</td><td>

Select the primary table for the project.

</td></tr><tr><td>

Relation

</td><td>

Relationships between tables can be either **Child** or **Reference**.

</td></tr><tr><td>

Source field

</td><td>

If you select the **Child** relation, then select a field from the child table that has a relation with the parent table.

 If you select the **Reference** relation, then the **Source field** is auto-populated.

</td></tr><tr><td>

Target Field

</td><td>

If you select the **Reference** relation, then select a field from the child table that has a relation with the parent table.

 If you select the **Child** relation, then the **Target field** is auto-populated.

</td></tr><tr><td>

Filters \(Optional\)

</td><td>

If required, you can set filters for the child table.

</td></tr><tr><td>

Related List Condition \(Optional\)

</td><td>

Displays the selected number of related records for the filters set. You can filter it further.

</td></tr></tbody>
</table>6.  Select **Save**.


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

