---
title: Define a PDF field mapping
description: Define editable fields and store signature mappings using the PDF field mappings section.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Document Templates of type PDF \(Advanced forms\), Configure, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Define a PDF field mapping

Define editable fields and store signature mappings using the PDF field mappings section.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

Information on the PDF is parsed and stored in the PDF Mapping table. **Parse PDF** will allow you to store the fillable fields and **Mark signatures** will allow you to add signature mappings.

## Procedure

1.  Navigate to **All** &gt; **Document Templates** &gt; **All Document Templates**.

2.  Select **PDF Document Template**.

3.  [Configure the PDF template.](configure-editable-pdf.md)

4.  Click the **Parse PDF** related link.

    **Note:** The link appears only for an editable PDF.

    The PDF Mapping related list displays field mappings.

<table id="table_zxn_bkx_xkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Display name that represents the document field.

</td></tr><tr><td>

PDF template

</td><td>

PDF template to which the mapping record belongs.

</td></tr><tr><td>

Document field

</td><td>

Field from the fillable PDF document that is automatically created through the **Parse PDF** related link. **Important:** Editing Document field is not allowed as it might break the document template flow.

</td></tr><tr><td>

Document field type

</td><td>

Type of field you are mapping, such as Signature or Checkbox.

</td></tr><tr><td>

Preview value

</td><td>

Field-mapping value for preview.**Note:** Use this field to test a field value without going through the process of mapping fields or creating a case to test your mappings. What you enter here appears while you preview the document.

</td></tr><tr><td>

Advanced script

</td><td>

Use to configure script fields for complex mapping of a field.For example, to map a Social Security Number from the HR Profile \[sn\_hr\_core\_profile\] table to a document and format it correctly, a script is used.

</td></tr><tr><td>

Mandatory

</td><td>

Mandatory field to be filled by the assigned participant.**Note:** This field is not applicable for document field of type checkbox.

</td></tr><tr><td>

Mapping table

</td><td>

Table that the mapped fields come from.

</td></tr><tr><td>

Read only

</td><td>

Option for enabling the editing of the field by the selected participant.

</td></tr><tr><td>

Mapping field

</td><td>

Field that maps information into your document.

</td></tr><tr><td>

Participant

</td><td>

Participant who can edit the field in the document.

</td></tr><tr><td>

Page number

</td><td>

Page number of the PDF document which contains the field. Page number where the field is present.

</td></tr><tr><td>

Format

</td><td>

Format in which values are to be entered by the participant. If the participant does not enter value in the specified format, a validation error appears for the participant.

</td></tr><tr><td>

Active

</td><td>

Option for activating the field mapping.

</td></tr><tr><td>

Use Signing date

</td><td>

Option to record the signature date automatically in the specified field in PDF document.**Note:** This option is applicable to ServiceNow Sign only.

</td></tr><tr><td>

Date offset type

</td><td>

Indicates if the date should be Before, On, or After the specified date. **Note:** This field appears only for a date field when the **Advanced script** option is deselected.

</td></tr><tr><td>

Date offset quantity

</td><td>

Measuring units for the offset such as days, weeks, or months.**Note:** This field appears only for a date field mapping when the **Advanced script** option is deselected. It appears only when the **Before** or **After** values are selected in the **Date offset type** field.

</td></tr><tr><td>

Date offset units

</td><td>

Number of units to offset.**Note:** This field appears only for a date field mapping when the **Advanced script** option is deselected. It appears only when the **Before** or **After** values are selected in the **Date offset type** field.

</td></tr><tr><td>

Select date format

</td><td>

Format for the date field. Values are:-   User date format: Indicates that the date format is picked from the participant's user preference.
-   Specific format: Indicates the format in which you want the participant to enter the date.


</td></tr><tr><td>

Specific date format

</td><td>

Specific format in which you want the participant to enter the date.

</td></tr><tr><td>

States

</td><td>

Options stored for the non text fields. For example, social status might includes options such as **Married** or **Single**.

</td></tr></tbody>
</table>
