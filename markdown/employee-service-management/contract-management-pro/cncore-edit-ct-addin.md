---
title: Edit a contract template using Microsoft Word add-in for ServiceNow Contracts
description: Edit the metadata, signatories, or clauses in a contract template that must be included in the contract template to generate a standard contract when an employee submits a contract request using the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage clauses, tables, and contract templates, Managing Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Edit a contract template using Microsoft Word add-in for ServiceNow Contracts

Edit the metadata, signatories, or clauses in a contract template that must be included in the contract template to generate a standard contract when an employee submits a contract request using the Microsoft Word add-in for ServiceNow Contracts.

## Before you begin

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open a Microsoft Word document that contains content controls.

2.  From the Microsoft Word ribbon, select ServiceNow Contracts add-in.

3.  Enter the credentials of the ServiceNow instance from where you downloaded the manifest file.

4.  In the Template tab, select the contract template that you want to modify.

    The associated contract template should be active and in Draft or Editing state.

5.  Modify the document.

<table id="table_rrc_vrb_gzb"><thead><tr><th>

Modification

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Modify the metadata, signatories, or clauses using the Microsoft Word add-in for ServiceNow Contracts.

</td><td>

[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

</td></tr><tr><td>

Edit or delete signatories.

</td><td>

[Edit or delete participants using add-in](../concept/cncore-del-signatory-addin.md)

</td></tr><tr><td>

Delete content controls

</td><td>

Right-click the content control and select **Remove Content Control**.The content control is deleted from the Microsoft Word document. However, you must upload and parse the document for content controls to be deleted from your ServiceNow instance.

</td></tr></tbody>
</table>6.  On finalizing the content controls, upload the document to the contract templates.

    1.  Select **Proceed to select a document**.

    2.  In the Select Attachment screen, select **Attach file** and select the modified document.

        If the file name of the document you are uploading and the one uploaded in the contract template are different, you are asked to confirm the upload.

    3.  Select **Upload and parse document** to parse the content controls and add the data to the ServiceNow instance.

7.  Complete clause mapping in the ServiceNow instance.

    For more information, see [Complete clause mapping to build a clause library](cncore-clause-map-addin.md).

    -   Unmodified existing metadata, signatories, and clauses are retained along with their details.
    -   Deleted metadata, signatories, and clauses are deleted from the Template mappings, Participants, and Imported clauses related lists of the contract template.
    -   Any added content controls are listed under Participants, Imported clauses, or Template Mappings.
8.  Select **Update**.

9.  On finalizing the content of the contract document, select **Publish**.


-   **[Edit or delete participants using add-in](../concept/cncore-del-signatory-addin.md)**  
As a contract configurator, edit or delete a participant from a Microsoft Word document using the Microsoft Word add-in for ServiceNow Contracts.
-   **[Edit or delete table mappings in a contract template using Microsoft Word add-in](cncore-manage-table-mappings.md)**  
As a contract configurator, edit or delete table mappings in a contract template using the Microsoft Word add-in.

**Parent Topic:**[Manage clauses, tables, and contract templates](../concept/cncore-manage-clauses-ctemplates.md)

**Related topics**  


[Edit a contract clause variation](cncore-edit-cv.md)

[Edit a contract template by manually adding content controls](cncore-edit-ct.md)

[Create a contract template from an existing template](cncore-create-template-revision.md)

[Generate and preview a contract document from a template](cncore-preview-template.md)

[Delete a contract template](cncore-delete-template.md)

