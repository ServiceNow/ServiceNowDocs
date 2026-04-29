---
title: Easy import template validation
description: Each import template must pass two sets of validation.Some cells in the template contain calculations or validation rules. These rules are intended to help you enter data that is appropriate for the field \(column\).Server-side validation verifies that the import template contains the necessary format.Both client-side and server-side validation verify that template cells contain data that matches the ServiceNow field type.
locale: en-US
release: australia
product: Easy Import
classification: easy-import
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Easy import, Imports, Workflow Data Fabric]
---

# Easy import template validation

Each import template must pass two sets of validation.

<table id="table_i3x_gq4_yq"><thead><tr><th>

Type of validation

</th><th>

Stored in

</th><th>

Results of failing validation

</th></tr></thead><tbody><tr><td>

Client-side validation

</td><td>

Import template

</td><td>

The template highlights the invalid cell.

 ![Import template client validation](../image/ImportTemplateClientValidation.png)

</td></tr><tr><td>

Server-side validation

</td><td>

Instance

</td><td>

The import pauses and displays an error message.

 ![Import template server validation](../image/ImportTemplateServerValidation.png)

</td></tr></tbody>
</table>**Parent Topic:**[Easy import](../concept/c_EasyImport.md)

## Template data validation

Some cells in the template contain calculations or validation rules. These rules are intended to help you enter data that is appropriate for the field \(column\).

If you want to paste data from another spreadsheet, use the Paste Special command to paste only values or match the existing formatting.

![](../image/EasyImportPasteSpecial.png "Easy import paste special")

![](../image/PasteSpecialValuesOnly.png "Paste special values only")

## Template type validations

Server-side validation verifies that the import template contains the necessary format.

<table id="table_mwz_hs4_yq"><thead><tr><th>

Template type

</th><th>

Validation done

</th></tr></thead><tbody><tr><td>

Insert template

</td><td>

-   Template contains a header row with valid field names.
-   Template contains one or more data rows.
-   Template does not contain a sys\_id column.

</td></tr><tr><td>

Update template

</td><td>

-   Template contains a header row with valid field names.
-   Template contains one or more data rows.
-   Template contains a sys\_id column to match a row to an existing record.

</td></tr></tbody>
</table>## Data type validations

Both client-side and server-side validation verify that template cells contain data that matches the ServiceNow field type.

<table id="table_phm_nt4_yq"><thead><tr><th>

ServiceNow field type

</th><th>

Validation done

</th></tr></thead><tbody><tr><td>

Choice list

</td><td>

Cell contains a value that matches a choice option from the choice list.

</td></tr><tr><td>

Integer

</td><td>

Cell contains a number without any decimal points.

</td></tr><tr><td>

Reference

</td><td>

Cell contains a value that matches an existing related record. This validation applies only to fields in which the list of possible choices is relatively small and mostly static. It does not apply to fields such as ‘Assigned To’ in which the list of possible choices is dynamic and large. Validation takes place when the data is inserted into the database, but not in Excel.**Note:** When you enter reference field values in the Excel spreadsheet, enter the display value and not the sys\_id of the referenced record. Enter this value the same as you would on a form. For example, for a reference to a user record, enter the username.

</td></tr><tr><td>

True \| False

</td><td>

Cell contains a true or false value.

</td></tr></tbody>
</table>