---
title: Field map script variables
description: Several predefined variables are available in the Source script field.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Field map script variables

Several predefined variables are available in the **Source script** field.

<table id="table_sly_ybg_r5"><thead><tr><th>

Variable

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The record from the source table that is currently being processed.

</td></tr><tr><td>

target

</td><td>

GlideRecord

</td><td>

The record from the target table that is currently being processed.

</td></tr><tr><td>

answer

</td><td>

String

</td><td>

The field value to set in the target record.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. Use this object to log messages such as `log.info("<Message>")` or `log.warn("<Message>")`. This object logs to the import log for standard import sets, or other log locations as required, such as for web service imports.

</td></tr><tr><td>

action

</td><td>

String

</td><td>

Contains either the value **insert** or **update**, depending on whether the current target row will be created or updated.**Note:** The *action* variable is available only when the **Coalesce** field is **false**.

</td></tr></tbody>
</table>**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

