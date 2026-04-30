---
title: Create a field map
description: Field maps establish a relationship between a field in an import set table and a field in the target table.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Importing data using import sets, Import sets, Imports, Creating integrations with applications]
---

# Create a field map

Field maps establish a relationship between a field in an import set table and a field in the target table.

## Before you begin

Role required: import\_transformer, import\_admin, or admin

## About this task

The field map determines what values from the source table the transformation adds to the target table.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Transform Maps**.

2.  Open a transform map.

3.  In the **Field Maps** related list, click **New**.

4.  Complete the form.

<table id="table_ajv_1hs_1gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Map

</td><td>

Transform map that uses this field mapping \(populated automatically\).

</td></tr><tr><td>

Source table

</td><td>

Table from which the raw import set data is loaded \(the source for the transformation\). Populated automatically from the transform map.

</td></tr><tr><td>

Source field

</td><td>

Field on the source table to be transformed. Can be blank if the **Source table** contains only raw data.

</td></tr><tr><td>

Choice action

</td><td>

Specifies the action to take if the import set contains a reference or choice value other than those available. Appears if the target field is a choice list or reference field.-   **create**: Create a new choice or record in the reference table.
-   **ignore**: Ignore the new value from the source table.
-   **reject**: Skip the entire row \(record\) containing the new value and continue to the next row.


</td></tr><tr><td>

Date format

</td><td>

Date format of the source field. Appears if the target field is a Date or Date/Time field.**Note:** To learn more about allowable date formats, see [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Use source script

</td><td>

Check box to use a script instead of the **Source field**.

</td></tr><tr><td>

Application

</td><td>

Application scope: global or per application.

</td></tr><tr><td>

Target table

</td><td>

Table in which the transformed data is inserted. You can select only tables within the currently selected application scope or the global scope, or tables that grant write access to other applications.

</td></tr><tr><td>

Target field

</td><td>

Field in the target table where the value from the source field is stored.

</td></tr><tr><td>

Referenced field value name

</td><td>

When the target field is a reference field, the transform map needs a way to match incoming source values to existing records in the reference field's source table. Since most imports do not provide a 32-character sys\_id value, you must specify a column from the reference field's source table that contains values that match the incoming source values.When there is a matching record, the transform map stores the sys\_id of the matching record in the target field. If there is no matching record, the transform map creates a new record in the reference field's table and stores the sys\_id of the new record in the target field.

 If you leave this field blank, the transform map looks for matching values from the display value column of the reference field table.

 For example, suppose you are importing incident records and the incoming data lists user IDs for the **Assigned to** field. If you leave **Referenced value field name** blank, the transform map searches for matching values in the User table's display value column: name. By setting the **Referenced value field name** to the user\_name column, you can match the user ID values to the appropriate user records.

</td></tr><tr><td>

Coalesce

</td><td>

Configuring a target field to coalesce causes the import set to treat the field as a unique key. When selected, the import set application attempts to match source values to records with values from an existing record. If a match is found, the transform map updates the record instead of creating a new record. When false, the import set application always creates new records for each transformation. If multiple fields are set to coalesce, all coalesce values must match an existing record. If two fields are set for coalescing and a matching value is found for one of the coalescing fields but not on the other, a new record is inserted.You must create an index on the target table if none of the coalesce fields are indexed. Indexing can improve performance for read and write operations. If one or more coalesce fields already has an index, you do not need to create an additional index.

 After setting the **Coalesce** value for all fields on the target table, use the **Index Coalesce Fields** related link to create an index. Before creating the index, ensure that the **Coalesce** value is set correctly for all fields on the target table to avoid creating unnecessary indexes for the same target table.

 The index needs to be concatenated; meaning all fields specified to be coalesced, need to be in the same index. The correct setup is for one index to include all fields being coalesced.

</td></tr><tr><td>

Coalesce empty fields

</td><td>

Check box to match an empty source field value to an empty target field value. For example, the User transform map coalesces on the email field. With this option selected, a source record containing an empty email address coalesces to a target record containing an empty email address.

</td></tr><tr><td>

Coalesce case sensitive

</td><td>

Check box to make case-sensitive coalesce values result in the creation of new records. By default, values marked as **Coalesce** are used in a case-insensitive lookup for existing records. Case-insensitive records update existing records only and do not cause the creation of new records.

</td></tr></tbody>
</table>5.  Click **Save**.

6.  Repeat steps 3-5 for each field mapping.

7.  Click **Update**.


**Parent Topic:**[Importing data using import sets](../../../administer/import-sets/concept/c_ImportDataUsingImportSets.md)

