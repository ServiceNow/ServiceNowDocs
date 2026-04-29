---
title: Define a dictionary override
description: Use a dictionary override to allow a field in a child table to have a different value or behavior than the same field in a parent table. For example, a dictionary override changes the default value of the priority field from 4 in the parent table to 5 in the Incident table.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dictionary overrides, Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a dictionary override

Use a dictionary override to allow a field in a child table to have a different value or behavior than the same field in a parent table. For example, a dictionary override changes the default value of the priority field from 4 in the parent table to 5 in the Incident table.

## Before you begin

Role required: admin.

## About this task

Dictionary overrides are only available for tables that support [table extension](../../table-administration/concept/table-extension-and-classes.md).

Dictionary overrides are inherited by extended tables, so it may be necessary to define additional overrides to change the value of fields on extended tables. For example, if you define the default value of cmdb\_ci.install\_status to be 3, and create an override for the same field on cmdb\_ci\_hardware to be 5, all tables extended from the Hardware table will also default to 5. So if you want the default cmdb\_ci\_computer.install\_status to be 3, you will need another override.

You can add a dictionary override in a scoped app, but you must add the override while working in the scoped app context and you can only select child tables from within that scope. Open the scoped app, edit the field’s dictionary entry, add a new dictionary override, select the child table, and then provide the override details.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the record for the field.

3.  In the **Dictionary Overrides** related list, click **New**.

4.  Fill in the fields on the form, as appropriate \(see table\).

<table id="simpletable_ph1_2hv_4q"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

The application scope to which the record belongs.

</td></tr><tr><td>

Base table

</td><td>

The parent table containing the field to override.

</td></tr><tr><td>

Table

</td><td>

Select the extended table to which the dictionary override applies.

 **Note:**

The list shows only tables and database views that are in the same scope as the dictionary override.

</td></tr><tr><td>

Override reference qualifier

</td><td>

Select the check box to display the **Reference qualifier** field, which overrides the [Reference qualifiers](../../../script/server-scripting/concept/c_ReferenceQualifiers.md) for the field on the extended table.

</td></tr><tr><td>

Override dependent

</td><td>

Select the check box to display the **Dependent** field, which overrides the field on which the current field depends.

</td></tr><tr><td>

Override attributes

</td><td>

Select the check box to display the **Attributes** field, which overrides the [dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md) for the field on the extended table.

 **Note:** Any attributes defined on the base table are ignored. If there are attributes on the base table that should still apply to the extended table, make sure to include them in this field.

</td></tr><tr><td>

Override default value

</td><td>

Select the check box to display the **Default Value** field, which overrides the default value for the field on the extended table.

</td></tr><tr><td>

Override calculation

</td><td>

Select the check box to display the **Calculation** field, which overrides the calculation of the value for the field on the extended table.

</td></tr><tr><td>

Override mandatory

</td><td>

Select the check box to display the **Mandatory** field, which overrides whether the field on the extended table must contain a value to save a record.

</td></tr><tr><td>

Override read only

</td><td>

Select the check box to display the **Read only** field, which overrides whether a user can change the field value on the extended table.

</td></tr><tr><td>

Override display value

</td><td>

Select the check box to use this field as the display value on the extended table.

 For example, the Story \[`rm_story`\] table uses the short description as the display value in reference fields instead of the number, as defined in the Task \[`task`\] table.

 **Note:** Only fields that exist at the task table can be used as display value overrides.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Dictionary overrides](../concept/c_DictionaryOverrides.md)

