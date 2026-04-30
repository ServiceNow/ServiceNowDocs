---
title: Updating records using coalesce
description: The coalesce option allows you to update existing target table records when transforming import data.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Import sets, Imports, Creating integrations with applications]
---

# Updating records using coalesce

The coalesce option allows you to update existing target table records when transforming import data.

The coalesce option on a field map allows you to specify if the selected **Target field** should be used to coalesce on when import set records are transformed. If the field map **Coalesce** checkbox is selected, when the import set row is transformed the instance checks for an existing record in the target table that has the same value in the **Target field** as the import set row **Source field**. For step-by-step instructions, see [Create a field map](../../../script/server-scripting/task/t_CreatingAFieldMap.md).

If an existing record with a matching value in the target table is found, that record is updated. If no matching record is found, then a new record is created in the target table.

**Note:** Choose fields in the target table to coalesce on only if those fields will have unique values. If more than one record in the target table matches the specified coalesce options, only the first matching record in the target table is updated.

## Coalesce options

There are several possible configurations you can use to coalesce data in import sets.

## No coalesce

If no coalesce is defined, all imported rows are treated as new records. No existing records are updated.

## Single-field coalesce

You can coalesce on a single field to update an existing record.

If a target table record exists with the same value in the coalesce field as the staging table record, the target table record is updated using the import set record values.

## Multiple-field coalesce

You can coalesce on multiple fields to update an existing record.

If a target table record exists with the same values in all coalesce fields as the staging table record, the target table record is updated using the staging table record values. All coalesce field values between the target and staging tables must match to coalesce with multiple fields.

## Conditional coalesce

You can use a script to determine if a staging table row should coalesce to a target record.

Most conditional coalesce scripts are defined in the **Source script** field of a field map for the sys\_id field. To update a target record using the staging table record values, the script must return the sys\_id of the target table record.

## Example conditional coalesce scripts

Review examples of conditional coalesce scripts.

## Updates only

To only update records where a match is found, and skip records where a match is not found, specify a coalesce field and add the following script as an **onBefore** script to the transform map.

```
if (action == 'insert') 
  ignore = true;
```

## Conditional coalesce using dot-walking

You can use dot-walked fields in a conditional coalesce script, such as to match the email address of a user when importing incident data.

In this example, this script is defined in the **Source script** of a field map for the Incident target table sys\_id field.

```
var gr = new GlideRecord('incident');
gr.addQuery('caller_id.email', source.u_email); //check if the incident caller's email matches the import row email value
gr.query();

if(gr.next())
{
    answer = gr.sys_id; //if a match exists, return the sys_id of the matching Incident record
}
else
{
    answer= -1;
}
```

## Conditional coalesce with an OR condition

You can use a conditional coalesce script to match source and target records based on multiple field values. Unlike multiple-field coalesce where all coalesce fields must match, you can specify a script to only require one of the fields to match.

In this example, this script is defined in the **Source script** of a field map for the User target table sys\_id field.

```
var gr = new GlideRecord('sys_user');
var qc = gr.addQuery('email', source.u_email); //first check if the user's email matches
qc.addOrCondition('user_name', source.u_name); //alternatively, check if the username matches
gr.query();

if(gr.next()) 
{
    answer = gr.sys_id; //if a match exists, return the sys_id of the matching User record
}
else 
{
    answer = -1;
}
```

## Case-sensitive coalesce field values

You can control if an import set will coalesce on matching values with different cases.

The field map **Coalesce case sensitive** field enables you to coalesce field values by case sensitivity.

By default, fields marked as **Coalesce** in the field map are used in a case insensitive lookup for existing records. If the **Coalesce case sensitive** check box is selected, the instance attempts to match coalesce field values by case. The target table record is updated only if the value in the target record and the import set staging record have the same value and case. Otherwise, a new record is created.

## Coalesce on empty fields

You can control if an import set will coalesce on fields with no value.

The field map **Coalesce empty fields** field allows you to coalesce on fields with no value.

By default, fields marked as **Coalesce** in the field map cause the import set to check for a target record with a field value that matches the value from the import set staging record. When **Coalesce empty fields** is selected for that field map, an empty value in the target record and import set staging record counts as a match for the purpose of coalescing.

For example, the User transform map coalesces on the email field. With the **Coalesce empty fields** option selected, a source record containing an empty email address coalesces to a target record containing an empty email address.

