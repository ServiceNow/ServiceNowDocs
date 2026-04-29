---
title: Create a legal contract template of type PDF
description: Create a document template of type PDF by uploading an editable and fillable PDF file.
locale: en-US
release: australia
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Legal contract templates, Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create a legal contract template of type PDF

Create a document template of type PDF by uploading an editable and fillable PDF file.

## Before you begin

Role required: admin

## About this task

Legal contract templates help you to create and organize standard contract templates along with fillable metadata placeholders. You can create templates of HTML, PDF and Microsoft Word types. In a PDF document template type, you can upload a fillable PDF file and map fields in the PDF file with fields in a table.

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Templates**.

2.  Select **New**.

3.  Select Create **PDF Document Template**.

4.  On the form, fill in the fields.

<table id="table_nbm_c44_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the template.

</td></tr><tr><td>

Table Name

</td><td>

Name of the table that contains the fields to include in the document template.Select **General Contract Support \[sn\_lg\_ops\_general\_contract\_support\]**.

</td></tr><tr><td>

Contract type

</td><td>

Contract type to which the template is associated.

</td></tr><tr><td>

Active

</td><td>

Option for marking the contract template as active.

</td></tr><tr><td>

User criteria

</td><td>

User criteria to control which users can use the document.

</td></tr><tr><td>

Document

</td><td>

Option to upload a fillable PDF for further customization. Click the **Click to add** link to upload a PDF file.

</td></tr></tbody>
</table>5.  Save the contract template.

    -   Save a contract template by clicking **Submit**.
    -   Save the changes to an existing contract template by clicking **Update**.
    The contract template is saved in the Draft state. Related lists to manage participants and to map PDF Template fields appear.

6.  Add participants in the contract template.

    1.  In the Participants related list, click **New**.

    2.  In the **Name** field, enter the display name for the participant.

        For example, for an internal signatory, you could enter `Internal Signer 1`.

    3.  In the **Order** field, enter the order in which the signature request will be initiated for the participant.

    4.  In the **Signer** field, select a user field from the list of fields that are populated from the Signer \[sn\_lg\_contracts\_signer\] table.

        **Note:** You can select only the highlighted user fields.

        The user in the mapped field is automatically added as a signatory in the document.

    5.  In the **User** field, select a user field from the list of fields that are populated from the Users \[sys\_user\] table.

    6.  Click **Submit**.

7.  Map a PDF field mapping to a field in the selected table.

    1.  Click the **Parse PDF** related link.

        **Note:** The related link appears only if the attached PDF file is editable.

        The editable fields from the attached PDF file are added in the PDF Template Mappings related list.

    2.  In the PDF Template Mappings related list, click **Field name** to open the field mapping.

    3.  On the PDF Template Mappings form, update the fields.

<table id="table_pdf_field_mapping"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Name that represents the field mapping and stored as part of the document mapping in the database.

</td></tr><tr><td>

PDF template

</td><td>

Name of the PDF template to which the mapping record belongs.

</td></tr><tr><td>

Document field

</td><td>

Field from the editable PDF file. **Warning:** Editing the document field might break the document template flow.

</td></tr><tr><td>

Document field type

</td><td>

Type of the mapping field.

</td></tr><tr><td>

Preview value

</td><td>

Value of the mapping field for preview.You can use this field to validate a field value that would appear in the generated document without creating a legal request to test your mappings.

</td></tr><tr><td>

Format

</td><td>

Format to enter values by the participant in the field.A validation error appears when the participant doesn't enter a value in the specified format.

</td></tr><tr><td>

Read only

</td><td>

Option for enabling the editing of the field by the selected participant.

</td></tr><tr><td>

Mandatory

</td><td>

Option for marking the field as required to be filled by the assigned participant.

</td></tr><tr><td>

Active

</td><td>

Option for marking the field mapping as active.

</td></tr><tr><td>

Mapping table

</td><td>

Table from which the mapping fields are referenced.

</td></tr><tr><td>

Mapping field

</td><td>

Field from the mapping table that maps to the field in the **Document field**.

</td></tr><tr><td>

Participant

</td><td>

User who can edit the field in the document.The list is populated from the Participants related list.

</td></tr><tr><td>

Advanced script

</td><td>

Option for using scripted fields for complex mapping of a field.On selecting, the **Script** field appears.

</td></tr><tr><td>

Script

</td><td>

Enter a script to configure script fields for a complex field mapping.

</td></tr></tbody>
</table>    4.  Click **Update**.

8.  Specify an area in the PDF document where you want to collect the signatures of the participants.

    1.  Click the **Mark Signatures** related link.

    2.  In the Mark Signature Blocks dialog box, click **Add Field**.

    3.  In the document preview pane, mark an area by dragging the mouse device.

    4.  In the **Name** field, enter a name for the signature-mapping record.

    5.  In the **Mapping** list, select a user as the signer.

        The list shows participants from the Participants related list.

    6.  Click **Save**.

9.  Click **PDF Preview** to preview the document.

10. To make the template available for usage, click **Publish**.


