---
title: Select a field as the table display value
description: Only one field can be defined as the display value for a table.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Display values, Reference field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Select a field as the table display value

Only one field can be defined as the display value for a table.

## Before you begin

Role required: personalize\_dictionary

## About this task

When you set the **Display** value to **true**, a business rule sets the **Display** value to **false** for all other fields on the table. In previous versions, you must manually ensure that no other fields on the table have a value of **true** in the **Display** column.

**Note:** Extended tables inherit the display value of the parent table. Setting a separate display value for the extended table overrides the parent table's display value.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Filter on **\[Table\] \[is\] \[&lt;name of the referenced table&gt;\]**.

3.  Locate the desired field and set **Display** to **true**.

    For best results, choose a field that is required and unique in each record as the display value field.

    **Note:** If you make a field the display field for a table, be sure to translate all values for the field in the Translated Text \[sys\_translated\_text\] table into all the languages provided. Display field options left untranslated are not presented by the autocomplete \(type ahead\) feature.

    Reference fields look for the display value in the following order:

    1.  A field with display=true in the system dictionary on the lowest sub-table for extended tables.
    2.  A field with display=true in the system dictionary on the parent table.
    3.  A field named **name** or **u\_name** or **x\_name**.
    4.  A field named **number** or **u\_number** or **x\_number**.
    5.  The field named in the Glide Property **glide.record.display\_value\_default**
    6.  The **Created on** field of the referenced record.

**Parent Topic:**[Display values](../concept/c_DisplayValues.md)

