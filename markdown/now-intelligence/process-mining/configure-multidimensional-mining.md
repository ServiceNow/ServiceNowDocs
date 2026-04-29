---
title: Configure multi-dimensional mining
description: Use multi-dimensional mining to identify inefficiencies and improve performance by evaluating data from multiple related tables.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up a table configuration, Create a project using Classic view, Use, Process Mining, Platform Analytics]
---

# Configure multi-dimensional mining

Use multi-dimensional mining to identify inefficiencies and improve performance by evaluating data from multiple related tables.

## Before you begin

You must install and configure Process Mining plugins before configuring multi-dimensional mining on tables.

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## About this task

Often the start and end of a full workflow occurs outside the life cycle of your business process. When it's helpful to analyze these external events, you can add another table for tracking other events relevant to your process. For example, if Incident table is your parent table, and you define the Incident Task \[incident\_task\] table as child table for the Incident table, then when a record from the Incident Task \[incident\_task\] table is created, it shows as an 'Incident Task created' activity on the process map. Only 'created' or 'closed' events show as activities in the process graph.

**Note:** External events from a defined child table don’t show as condition options in the Transitions or condition filters.

## Procedure

1.  Select the project for which you want to configure multi-dimensional mining.

2.  Go to the **Table Configuration** tab, and select **New**.

    **Note:** The project must already have a parent table configuration set up.

    A new table configuration page is displayed.

    ![Add child table](../image/multi-dimension-2.png)

3.  Provide a name for the child table configuration in the **Name** field.

4.  In the **Step 1** section, provide details as you would do for table configuration.

    For more information, see [Set up a table configuration](po-table-configuration.md).

5.  To set a relationship, fill the fields in the **Step 2** section.

<table id="table_ir5_v5f_2vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Parent Table Configuration

</td><td>

Select the search icon next to **Parent Table Configuration**, and select the parent table configuration.

</td></tr><tr><td>

Relationship

</td><td>

Select **Reference** or **Child** from the drop-down list of **Relationships**, depending on the relation type.

 A reference field stores a reference to a field on another table. For example, the **Problem** field on the Incident table is a reference to the Problem table. Child records are related with a particular parent record. For example, requested items have service catalog tasks or incidents and SLA records.

</td></tr><tr><td>

Source Field

</td><td>

If you select the **Child** relation, then select a field from the child table that has a relation with the parent table.

 If you select the **Reference** relation, then the **Source field** is auto-populated.

</td></tr><tr><td>

Target Field

</td><td>

If you select the **Reference** relation, then select a field from the child table that has a relation with the parent table.

 If you select the **Child** relation, then the **Target field** is auto-populated.

</td></tr></tbody>
</table>6.  Select **Submit**.

    A new child table configuration is created.

    Configure an activity definition for the table configuration. For more information, see [Configure an activity definition](configure-activity.md).


**Parent Topic:**[Set up a table configuration](po-table-configuration.md)

