---
title: Update contract template mappings for legal contract template
description: Update template mappings to pre-fill information that will be placed in the contract document.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure legal contract templates of type Microsoft Word, Legal contract templates, Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Update contract template mappings for legal contract template

Update template mappings to pre-fill information that will be placed in the contract document.

## Before you begin

Role required: sn\_lg\_contracts.contracts\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Templates**.

2.  Open a contract template.

3.  Navigate to the Template mapping related list.

4.  Select the field to update.

5.  On the form, fill in the fields.

<table id="table_u4t_fyh_f3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

This field is automatically populated with the title of content control. For example: Company

</td></tr><tr><td>

Document field

</td><td>

This field is automatically populated with the tag of the content control. The field has the field type prefixed to the name. For example: field\_companyName.

</td></tr><tr><td>

Document field type

</td><td>

The type of field being mapped. The choices are:-   Text Field: A placeholder for metadata.
-   Signature: A placeholder for signatures during the electronic signature process.
-   Signature date: A placeholder for the date of the signing.


</td></tr><tr><td>

Preview value

</td><td>

A field mapping value used instead of the placeholder when testing the template. This field appears only when **Text field** is selected from **Document field type**.

</td></tr><tr><td>

Format

</td><td>

Format in which values are to be entered by the participant. A validation is displayed if the entered value does not match the specified format, This field appears only when **Text field** is selected from **Document field type**.

</td></tr><tr><td>

Read Only

</td><td>

Option for enabling the editing of the field by the selected participant.

</td></tr><tr><td>

Active

</td><td>

Option for activating the template mapping.

</td></tr><tr><td>

Mapping table

</td><td>

This field is automatically set to the table to which the document template is associated.

</td></tr><tr><td>

Mapping field

</td><td>

Mapping field used to map the values from the table field that will be inserted when this template is used in a contract. This field appears only when **Text field** is selected from **Document field type**.

</td></tr><tr><td>

Participant

</td><td>

Select the participant associated with the contract template.-   If **Document field type** is set to **Text field**, the selected participant is responsible for the task.
-   If **Document field type** is set to **Signature**, the selected participant is responsible for signing the document.
-   If **Document field type** is set to **Signature date**, the date of signing by the signatory will be placed in the document.


</td></tr><tr><td>

Advanced script

</td><td>

Option to display the Script editor.

</td></tr><tr><td>

Script

</td><td>

Script configuring the mapping between fields and record producer variables. This field is enabled only when the **Advanced script** field is selected.

</td></tr></tbody>
</table>6.  Select **Update**.


**Parent Topic:**[Configure legal contract templates of type Microsoft Word](lsc-configure-ct-msword.md)

**Related topics**  


[Add content controls in a Microsoft Word document](lsc-cont-contr-word-tmplt.md)

[Create a Microsoft Word legal contract template](lsc-create-ct-msword.md)

[Create and configure participants for legal contract template](lsc-add-config-participants-msword.md)

[Publish a contract template](lsc-publish-word-template.md)

