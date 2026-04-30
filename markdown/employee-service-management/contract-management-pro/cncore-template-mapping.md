---
title: Update contract template mappings
description: Update template mappings to pre-fill information that's placed in the contract document.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create contract template by manually adding content controls, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Update contract template mappings

Update template mappings to pre-fill information that's placed in the contract document.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

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

This field is automatically populated with the title of the content control. For example: Company

</td></tr><tr><td>

Document field

</td><td>

This field is automatically populated with the tag of the content control. The field has the field type prefixed to the name. For example: field\_companyName.

</td></tr><tr><td>

Document field type

</td><td>

The type of field being mapped. The choices are:-   Text Field: Descriptive metadata.
-   Signature: Signatures during the electronic signature process.
-   Signature date: Date of the signing.
-   Signatory name: Name of the signatory.
-   Signatory email: Email of the Signatory.
-   Signatory title: Title of the signatory.
**Note:**

-   These options are available when the template is contracts-related for Contract Management Pro.
-   Ensure you have mapped Signature and Signature date to the participants and delete any unmapped Signature and Signature date fields.


</td></tr><tr><td>

Preview value

</td><td>

A field mapping value used instead of the placeholder when testing the template. This field appears only when **Text field** is selected from **Document field type**.

</td></tr><tr><td>

Format

</td><td>

Format in which values are to be entered by the participant. If the participant doesn’t enter a value in the specified format, a validation error appears for the participant.

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

Mapping field used to map the values from the table field that is inserted when this template is used in a contract. This field appears only when **Text field** is selected from **Document field type**.

</td></tr><tr><td>

Participant

</td><td>

Select the participant associated with the contract template.While creating of participants,

-   To create an internal signer, map user reference to the participant record, for example, P1.
-   To create an external signer, map the Participant name, Participant email, and Participant title fields in the participant record.
When you map a participant to signatory name, email, and title fields in the template mappings, the participant record mapped value to the participant name, email, and title fields in the signer tasks.

**Note:** When the template has a signatory rule, the signer mapping under the signatory rule takes precedence over the user mapping in participant record.

</td></tr><tr><td>

Advanced script

</td><td>

Option to display the Script editor.

</td></tr><tr><td>

Script

</td><td>

The script configuring the mapping between fields and record producer variables. This field is enabled only when the **Advanced script** field is selected.

</td></tr></tbody>
</table>6.  Select **Update**.


**Parent Topic:**[Create contract template by manually adding content controls](../concept/cncore-setup-ct-manual.md)

**Related topics**  


[Add content controls in a Microsoft Word document](cncore-word-doc-tmplt-contls.md)

[Create a contract template](cncore-create-contract-template.md)

[Create and configure participants](cncore-add-participants.md)

[Classify and map imported clauses](cncore-import-clauses.md)

