---
title: Add or modify a PDF template mapping
description: With PDF template mapping you can pre-fill information from specified tables into a reuseable HR document configured in a PDF document template.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure an HR PDF document template, HR document templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Add or modify a PDF template mapping

With PDF template mapping you can pre-fill information from specified tables into a reuseable HR document configured in a PDF document template.

## Before you begin

Role required: sn\_hr.core\_admin

## About this task

**Important:**

Starting with the Xanadu release, HR Document Templates is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported.

Use [Document Templates](../concept/document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](../concept/migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

PDF template mappings are derived from the table associated with the PDF document template. PDF template mapping is accessed from a PDF document template that contains fields that can be mapped. Refer to [Configure an HR PDF document template](PDFTemplate.md).

The PDF Template Mappings section appears when a new fillable PDF document has been uploaded from Managed Documents and the **Parse PDF** link is selected.

## Procedure

1.  Select a field to edit.

2.  Complete the form.

<table id="table_u4t_fyh_f3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Enter a name that represents the field mapping and stored as part of the document mapping in the database.

</td></tr><tr><td>

HR PDF template

</td><td>

The name of the PDF template associated with the field mapping.

</td></tr><tr><td>

Document field

</td><td>

The field that appears in the document template. Typically the same name as the **Field name** but can be different. For example, on an I-20 document template, a **Document field** is \#form\[0\].First Name. But, the **Field name** can be First Name.

</td></tr><tr><td>

Document field type

</td><td>

Select the type of field you are mapping. The choices are:-   Signature
-   Text Field
-   Checkbox
-   Combo
-   Radio


</td></tr><tr><td>

Preview value

</td><td>

Enter a field mapping value for preview. **Note:** Use this field to test a field value without going through the process of mapping fields or creating a case to test your mappings. What you enter here appears in your document.

</td></tr><tr><td>

Advanced script

</td><td>

Use to configure script fields for complex mapping of a field. For example, to map a Social Security Number from the HR Profile \[sn\_hr\_core\_profile\] table to a document and format it correctly, a script is used.

</td></tr><tr><td>

Mapping table

</td><td>

The table that the mapped fields come from.

</td></tr><tr><td>

Mapping field

</td><td>

The field that maps information into your document.

</td></tr><tr><td>

Use signing date

</td><td>

Check when the signing date should be captured with the signature when a user signs the document.

</td></tr><tr><td>

Page number

</td><td>

The page number of the PDF document where the mapped field should insert information. For example, enter 2 when the mapped field appears on page 2 of the PDF document.

</td></tr><tr><td>

Active

</td><td>

Check to activate the field mapping.

</td></tr><tr><td>

Select date format

</td><td>

Appears when **Use signing date** is checked.Specify the date format to be used on a document.

 -   User date format: Uses date format specified on the User \[sys\_user\] table for the logged in user.
-   Specific date format: When selected, the Specific date format appears. Click the **Suggestion** icon and you can select from a list of formats.


</td></tr></tbody>
</table>3.  Click **Save** to save your field mapping and remain on the HR PDF Template form, or click **Submit** to save your field mapping and return to the HR Document Templates list.


