---
title: Create the normalization record
description: Regardless of the normalization method selected, all field normalization requires a list of existing variants and a normal value that is configured to replace these variants in forms and in queries.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Normal values, Field normalization and transformation, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create the normalization record

Regardless of the normalization method selected, all field normalization requires a list of existing variants and a normal value that is configured to replace these variants in forms and in queries.

## About this task

Normalize a field by selecting aliases for a normal field value or by creating rules that use condition statements to match field variants with a normal value.

**Note:** Users must have the normalizer role to create and manage normalization records.

Special Cases

-   Reference fields cannot be normalized. To normalize values appearing in reference fields, normalize the field in the target table. Examples of this would be normalized values for the **Name** fields in the Company \[core\_company\] and Location \[cmn\_location\] tables, which are referenced by other tables in the platform. The normalized names are available to all fields that reference these tables.
-   Fields in a choice list can be normalized if they are of a type **string**.

## Procedure

1.  [Activate](../../plugins/task/t_ActivateAPlugin.md) the Field Normalization plugin.

2.  Navigate to **Field Normalization** &gt; **Configurations** &gt; **Normalizations**.

3.  Click **New**.

4.  Create a normalization record.

    |Field|Input value|
    |-----|-----------|
    |Name|Unique name for this normalization record. This value is for reference only and is not used in any processing.|
    |Table|Select the ServiceNow table for the field being normalized.|
    |Field|Select the field to normalize.|
    |Mode|The three available modes are Off, Test, and Active. All normalization records are created in the test mode by default. If you are planning to select aliases for your normal values, change the Mode to Active. If you intend to normalize the field using rules, be sure to leave this record in the Test mode. To disable this normalization, switch the mode to Off.|
    |Normalize query|Select this check box to apply the field value normalized by this record to all queries involving this field. Queries formed with the raw \(original\) field value return records displaying the normal value. Queries issued by a script using the conditions equals or not equals return normalized values. See [Normalized Queries](../concept/c_WhatFieldNormalizationDoes.md) for details.|
    |Coalesce each normal|Select this check box to normalize reference field values. This option resets all references to records containing an alias field value to the record using the normal value. See [Coalesce Normal Values](t_CoalesceNormalValues.md) for details.|
    |Raw field|Select the field to use to display the original \(non-normalized\) input values on a form in which a field value has been normalized. For the selection to appear in the drop-down list, add a custom field to the form for the table selected. For instructions on adding a field for raw data, see [Creating a Raw Field](t_CreateARawField.md).|

    After the normalization record is submitted, the platform runs the Pending value collection job in the **Data Jobs** related list automatically to gather all the current values \(Pending Values\) for the field being normalized.

    ![Run data job](../image/NormalizeForm1.png)

    Click the **Pending Values** related list to view values for the normalized field that have been entered manually, imported into the platform, or created by Discovery.

    ![Pending values list](../image/NormalizeForm2.png)


