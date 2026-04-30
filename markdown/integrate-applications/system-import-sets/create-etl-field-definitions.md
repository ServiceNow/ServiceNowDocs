---
title: Create ETL entity field definitions
description: Define the entity fields mapped for Extract Transform Load \(ETL\) operations.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create Extract Transform Load \(ETL\) definitions, Robust Import Set Transformers, Import sets, Imports, Creating integrations with applications]
---

# Create ETL entity field definitions

Define the entity fields mapped for Extract Transform Load \(ETL\) operations.

## Before you begin

Role required: import\_transformer

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **ETL Definitions**.

2.  Select an ETL definition.

3.  On the ETL Entities tab, select an ETL entity.

4.  On the ETL Entity fields tab, click **New**.

5.  Complete the form.

<table id="table_qcb_bmv_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ETL Entity field definition.

</td></tr><tr><td>

Field/Path

</td><td>

The column name in the staging or import set table.

 For reference fields in a target entity, you can specify the columns to map data to. For example, suppose you're mapping data to an address table with three columns: number, street, and postal code. You can specify the unique column to map to by entering `address.number`, `address.postal_code`, and `address.street`.

 When specifying unique columns in reference fields, all must have the same coercion action and coalesce value. For example, all three address fields listed previously must have the same coercion action and the same coalesce value.

 For an import entity, a field within an array can be referenced with the \[\*\] notation. For example, for the following nested structure, you can specify the email address by entering `emails[*].address`.

```
{
      "id": "123",
      "name": "Jhon",
      "emails": [
        {
          "address": "jhon@servicenow.com",
          "type": "work"
        },
      ]
    }

```

</td></tr><tr><td>

Coercion action

</td><td>

What the system should do if a reference or choice could not be found. Available options are create, ignore, and reject.-   For the create option, the system creates a new reference/choice and assigns it to the current record.
-   The ignore option sets the current value as empty.
-   The reject option does not save the whole record to the database.


</td></tr><tr><td>

Coalesce

</td><td>

Use this field to query the existing records.

</td></tr><tr><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

Entity

</td><td>

Name of the robust transform engine entity.

</td></tr><tr><td>

Definition

</td><td>

Selected ETL entity that this field definition belongs to.

</td></tr></tbody>
</table>6.  Click **Submit**.


