---
title: Configure rollup for planned task fields
description: You can configure the planned task fields to roll up the field values in the parent entity.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Planned tasks, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure rollup for planned task fields

You can configure the planned task fields to roll up the field values in the parent entity.

## Before you begin

Role required: admin

## About this task

By default the following fields are configured to roll up for any planned task and planned task derivatives:

**Cost**, **Budget**, **Effort**, **Actual date**, **Planned date**, **Duration**, **Percent Complete**

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open the **Planned task rollup** table.

3.  In the Related links, click **Show List**.

4.  Click **New**.

5.  Fill out the Planned task rollup form \(see table\).

6.  Click **Submit**.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Child

</td><td>

Select the table you want to include or exclude.

</td></tr><tr><td>

Field

</td><td>

Select the column name you want to include or exclude.

</td></tr><tr><td>

Navigator

</td><td>

The reference column of the parent to which the value must be rolled up.

</td></tr><tr><td>

Parent

</td><td>

Select the parent table.

</td></tr><tr><td>

Application

</td><td>

Auto-generated value.

</td></tr><tr><td>

Rollup

</td><td>

Select the check box to allow roll up. Leave the field unchecked to exclude the field from rollup.

</td></tr></tbody>
</table>
**Parent Topic:**[Extending the Task table with Planned tasks](../concept/c_PlannedTask.md)

