---
title: Show reference fields as lists in Excel templates
description: Display selected reference fields as lists in Excel templates to simplify data selection and updates.
locale: en-US
release: xanadu
product: Easy Import
classification: easy-import
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Easy import, Imports, Creating integrations with applications]
---

# Show reference fields as lists in Excel templates

Display selected reference fields as lists in Excel templates to simplify data selection and updates.

## Before you begin

When you do an Easy Import and export the data to an Excel spreadsheet, you may want to convert some cells to lists. For example, in the Incident \[sys\_incident\] record, you may want the **Assigned to** field options to appear as a list to enable you to select or update the person assigned to the incident.

Role required: admin

## Procedure

1.  Navigate to the record for which you want to create lists.

2.  Go to the field you want to appear as a list.

3.  Right-click the field name and select **Configure Dictionary**.

4.  In the **Attributes** field of the Dictionary Entry page, enter the following attribute: `easy_import_ref_as_choice=true`.

5.  Save your dictionary entry.

    You can also enter other **Attributes** for the dictionary entry. For example, there is a default limit of 250 entries in a list. If there are more than 250 entry options for a field, the entries do not appear in list format, but as a single entry. Assume that there are 500+ entry options. You can enter the following attribute in the dictionary entry for a field to set a higher limit of 600 entry options for that field: `easy_import_ref_query_limit=600`. The Excel spreadsheet now displays the field as a list of up to 600 options.

    You can set a system-wide limit for the number of entry options at a field by entering a value for the **glide.easy\_import.reference\_query\_limit** system property. If the system property is not present or not set and the `easy_import_ref_query_limit` attribute is not set for the field, the default limit of 250 entry options applies. The attribute always takes priority over the property: If both the attribute and the property are set, the attribute value is used.

6.  Repeat steps 2-4 for any other fields you want to appear as lists in the Excel output.

    The field appears as a list on the Excel spreadsheet:

    ![Excel choice list](../../key-management-framework/image/excel-list.png)


**Parent Topic:**[Easy import](../concept/c_EasyImport.md)

