---
title: Create a transform map
description: Every import operation to a production table requires at least one transform map associated with an import set.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Create a transform map

Every import operation to a production table requires at least one transform map associated with an import set.

## Before you begin

Role required: import\_transformer, import\_admin, or admin

## About this task

The transform map specifies the data relationships between the import set and the target table. For every transformation, you must either create a new transform map or select an existing one.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Create Transform Map**.

2.  Complete the form.

<table id="table_mbl_c2s_1gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

User-friendly label to identify the transform map.

</td></tr><tr><td>

Source table

</td><td>

Import table containing the raw import set data. An import table is any table that extends the Import Set Row `[sys_import_set_row]` table. You can select only tables within the currently selected application scope.

</td></tr><tr><td>

Active

</td><td>

Check box to make the transform map available for use.

</td></tr><tr><td>

Run business rules

</td><td>

Check box to run business rules, workflows, approval engines, auditing, and field normalization while the transformation inserts or updates data into the target table. Clearing this check box runs GlideRecord.setWorkflow\(\) with a value of **false**.

</td></tr><tr><td>

Enforce mandatory fields

</td><td>

Selects whether to enforce mandatory fields on the target table:-   **No**: Do not enforce mandatory fields.
-   **Only Mapped Fields**: Enforce mandatory mapped fields only.
-   **All Fields**: Enforce all mandatory fields.


</td></tr><tr><td>

Copy empty fields

</td><td>

Check box to copy empty field values and override existing target field values.

</td></tr><tr><td>

Create new record on empty coalesce fields

</td><td>

Check box to create a new record when all coalesce fields are empty, instead of ignoring the record or overwriting an existing record.If **Coalesce empty fields** is selected for any field in the record, the record is coalesced.

</td></tr><tr><td>

Application

</td><td>

Application scope: global or per application.

</td></tr><tr><td>

Created

</td><td>

Transform map creation date \(populated automatically\).

</td></tr><tr><td>

Target table

</td><td>

The table in which you want the transformed data to be inserted. You can select only tables within the currently selected application scope or the global scope, or tables that grant write access to other applications.

</td></tr><tr><td>

Order

</td><td>

Order in which to apply transform maps if more than one map fits the conditions. The system runs transform maps from lowest to highest **Order**.

</td></tr><tr><td>

Use Secondary Storage for References

</td><td>

Option to use a secondary database to look up reference fields.

 Importing a high volume of data that includes many reference fields might cause performance issues. Using secondary storage enables some read queries to be redirected to a secondary database, reducing the load on the primary database.

 When using secondary storage, set the **Choice action** field in the field map to **ignore** or **reject**. Setting the **Choice action** to **create** may cause multiple copies of a record to be created because the reference resolution doesn't detect newly created records immediately. For more information, see [Create a field map](t_CreatingAFieldMap.md).

 A secondary database is always slightly out of date compared to the primary database. If your import requires completely up-to-date data, don't use secondary storage.

 This field appears only when the Secondary Database Pools \[com.glide.secondary\_db\_pools\] plugin has been activated, and the import\_reference\_resoultion secondary database category has been configured and enabled. For more information, see [Large data imports with many reference fields](../../../administer/technical-best-practice/concept/c_TroubleshootImportSetPerformance.md#).

</td></tr><tr><td>

Run script

</td><td>

Check box to define a script that transforms field values in the source table to the target table.

</td></tr><tr><td>

Script

</td><td>

Transform map script that transforms field values in the source table to the target table. The system runs the transform map script in addition to any field maps.

</td></tr></tbody>
</table>    **Important:** The string `NULL` is a reserved word. It should not be used as a field value in import set transform maps or anywhere in the **First name** or **Last name** fields. The reserved word is `NULL` in all capital letters. A field with the value `Null` or `null`, for example, is acceptable. `NULL` should be used only to clear out a particular field.


**Parent Topic:**[Importing data using import sets](../../../administer/import-sets/concept/c_ImportDataUsingImportSets.md)

