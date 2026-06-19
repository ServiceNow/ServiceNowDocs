---
title: Apply table extension
description: Preserve data sets using table extension.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/t\_TableExtensionExample.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Table extension, Applying database rotation techniques, Manage data growth, Data Management, Tables and data, Configure core features, Administer]
---

# Apply table extension

Preserve data sets using table extension.

## Before you begin

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

The type of rotation. Select **Extension**.

</td></tr><tr><td>

Duration

</td><td>

The days and hours during which data is written to each shard.

</td></tr></tbody>
</table>4.  Select **Submit**.

    \[Omitted image "TableExtension.png"\] Alt text: New table extension


## Result

A schedule is created and new shards are added indefinitely to preserve data.

**Note:** Deleting a rotation deletes the additional tables and all the data. Do not delete the rotation if you still need the data.

**Parent Topic:**[Table extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/table-extension.md)

