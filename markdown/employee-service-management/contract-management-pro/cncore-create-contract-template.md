---
title: Create a contract template
description: Create a contract template that can be used to generate a standard contract with predefined content when an employee submits a contract request.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create contract template by manually adding content controls, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Create a contract template

Create a contract template that can be used to generate a standard contract with predefined content when an employee submits a contract request.

## Before you begin

Role required: sn\_cm\_core.contract\_config

If you are creating a contract template for a non-task table, ensure that the non-task table is added in the extension script. For more information, see [Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md).

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

    The Word Templates page opens in the Contract Templates view by default.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_qfw_c4s_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the contract template.

</td></tr><tr><td>

Table

</td><td>

Table to which you want to associate the contract template.

</td></tr><tr><td>

Category

</td><td>

Document category to which you want to associate the contract template.

</td></tr><tr><td>

Document

</td><td>

The document from which you want to import clauses and template field mapping. The selected document should be a Microsoft Word \(.docx\) document and should have valid content controllers. For more information, see [Add content controls in a Microsoft Word document](cncore-word-doc-tmplt-contls.md).

</td></tr><tr><td>

State

</td><td>

Current state of the document template.-   **Draft**: Indicates that the document template is not yet published.
-   **Editing**: Indicates that the document template is being edited after it has been published.
-   **Published**: Indicates that the document template can be consumed by services and cases.


</td></tr><tr><td>

Application

</td><td>

Application to which the contract template belongs. This field is automatically set to the application scope in which you’re creating the contract template.

</td></tr><tr><td>

Active

</td><td>

Option to make the template active and available for use.

</td></tr><tr><td>

Start date

</td><td>

Date on which the Word document template becomes valid. Providing a start date helps when maintaining multiple versions of same template.This field is available only when **Category** is selected.

</td></tr><tr><td>

End date

</td><td>

Date until which the Word document template is valid. Providing an end date helps when maintaining multiple versions of same template.

 If the values in the **Start date** and **End date** fields are empty the template will always be valid.

 **Note:**

If you specify an end date, you must also specify a start date.

 This field is available only when **Category** is selected.

</td></tr></tbody>
</table>    When the document is selected, the Participants, Imported Clauses, Clause Mappings, and Template Mappings related list appear.

4.  In the **Contract Type** field, select only one category of the contract type.

    If you’re creating a template for non-disclosure agreement, select **Non Disclosure Agreement** as the contract type.

5.  Select **Parse Document** to extract the content marked by content control from the imported document.

    -   The content controls that have **clause\_** as prefix are derived from the document and listed under the Imported clauses related list.
    -   The content controls that have **field\_**, **signatory\_**, **signature\_**, and **sign\_** as prefix are derived from the document and listed under the Template mappings related list.
6.  Select **Save**.


## Result

The contract template is saved in the Draft state.

## What to do next

1.  To add participants with whom you must obtain signatures, see [Create and configure participants](cncore-add-participants.md).
2.  To insert signatures, open a **Signature\_** record in the **Template mappings** related list. For more information, see [Update contract template mappings](cncore-template-mapping.md)

    1.  In **Document field type**, specify `Signature`.
    2.  In the **Participant** field, specify the participant with whom you require the signature.
    3.  Select **Update**.
    Similarly, update the following records.

    -   Sign
    -   Sign date
    -   field
    -   Signatory name
    -   Signatory email
    -   Signatory title
    For a full list, see [Add content controls in a Microsoft Word document](cncore-word-doc-tmplt-contls.md)

3.  Select **Publish**.

**Parent Topic:**[Create contract template by manually adding content controls](../concept/cncore-setup-ct-manual.md)

**Related topics**  


[Add content controls in a Microsoft Word document](cncore-word-doc-tmplt-contls.md)

[Create and configure participants](cncore-add-participants.md)

[Classify and map imported clauses](cncore-import-clauses.md)

[Update contract template mappings](cncore-template-mapping.md)

