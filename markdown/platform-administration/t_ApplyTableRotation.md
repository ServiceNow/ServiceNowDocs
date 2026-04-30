---
title: Apply table rotation
description: Preserve instance performance by applying table rotation.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Table rotation, Applying database rotation techniques, Manage data growth, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Apply table rotation

Preserve instance performance by applying table rotation.

## Before you begin

Determine the type of table you have and whether you can apply table rotation yourself.

-   You can apply table rotation to custom tables that begin with a u\_ prefix at your own discretion.
-   Do not apply table rotation to scoped tables that begin with an x\_ prefix without consulting ServiceNow or the third-party plugin developer first.
-   Do not apply table rotation to out-of-the-box tables that begin with a sys\_ prefix. Contact Customer Service and Support for help with these tables.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Table Rotations**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_mfs_qhy_dq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the table.

</td></tr><tr><td>

Type

</td><td>

The type of rotation. Select **Rotation**.

</td></tr><tr><td>

Rotations

</td><td>

The number of tables to maintain through the duration.

</td></tr><tr><td>

Duration

</td><td>

The days and hours during which data is written to each shard.

</td></tr><tr><td>

Clean base rotation

</td><td>

The date to clean \(truncate\) the base table.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

A schedule is created and new data is written to one of the tables in the rotation group. The group includes the original table plus several additional tables.

**Note:** Deleting a rotation deletes the additional tables and all the data. Do not delete the rotation if you still need the data.

## New table rotation group

![New table rotation group.](../image/NewTableRotationGroup.png)

**Parent Topic:**[Table rotation](../concept/c_TableRotation.md)

