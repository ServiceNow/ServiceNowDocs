---
title: Create global rank column for high-level planning
description: Create a global rank column for planning item types that do not extend the Planning Item \[sn\_align\_planning\_item\] table so that you can enable high-level planning for these items in Strategic Planning Workspace.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [High-level planning configuration in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create global rank column for high-level planning

Create a global rank column for planning item types that do not extend the Planning Item \[sn\_align\_planning\_item\] table so that you can enable high-level planning for these items in Strategic Planning Workspace.

## Before you begin

Upgrade to Strategic Planning v2.1.0.

Role required: admin

## About this task

Create a **Global rank** column on the planning item table for which you want to enable high-level planning. This column allows populating a global rank for all existing and new records of this table in your ServiceNow instance.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Search for and open your planning item table.

    For example, search for and open the Strategic Priority \[sn\_gf\_strategy\] table.

3.  From the Columns related list, select **New**.

4.  On the form, fill in the following fields.

<table id="table_t55_npd_bxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table for which you are creating this column.

 This field is automatically set to the table you've selected in Step 2.

</td></tr><tr><td>

Type

</td><td>

Value type of the column that you're creating.

 Select **Long**.

</td></tr><tr><td>

Column label

</td><td>

Label for the rank column. Enter **Global rank**.

</td></tr><tr><td>

Column name

</td><td>

Auto-generated unique name for the column.

</td></tr><tr><td>

Application

</td><td>

Application scope of the table.This field is populated automatically based on the table that you selected.

</td></tr></tbody>
</table>    For complete details of the Dictionary Entry form fields, see [Dictionary entry form](https://www.servicenow.com/docs/access?context=r_DictionaryEntryForm&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

5.  Save the form.


## What to do next

Create a rank configuration for the global rank field you created. See [Create rank configuration for high-level planning](create-rank-configuration-enable-high-level-planning.md).

