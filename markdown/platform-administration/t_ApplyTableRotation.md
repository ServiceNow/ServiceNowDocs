---
title: Apply table rotation
description: Preserve instance performance by applying table rotation.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Table rotation, Database rotation, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
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

The type of rotation. -   Rotation and Extension are time-based.
-   Shard is based on a document ID.
See [Database rotation](../../database-rotation/concept/c_DatabaseRotation.md) for more information.

</td></tr><tr><td>

Rotations

</td><td>

The number of tables to maintain through the duration. Applies to **Rotation** type.

</td></tr><tr><td>

Duration

</td><td>

The overall duration for the action.Applies to **Rotation** and **Extension** type.

</td></tr><tr><td>

Clean base rotation

</td><td>

The date to clean \(truncate\) the base table.Applies to **Rotation** type.

</td></tr></tbody>
</table>4.  Select **Submit**.

    **Note:** Deleting a rotation deletes the additional tables and all the data. Do not delete the rotation if you still need the data.

    When you define a new rotation, a schedule creates and new data writes to one of the tables in the rotation group. The group includes the original table plus several additional tables.

    ![New table rotation group](../image/NewTableRotationGroup.png)


**Parent Topic:**[Table rotation](../concept/c_TableRotation.md)

