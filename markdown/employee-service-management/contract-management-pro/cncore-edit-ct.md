---
title: Edit contract templates by manually adding content controls
description: Edit a contract template to reflect any modifications that must be included in the template to generate a standard contract when an employee submits a contract request.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage clauses, tables, and contract templates, Manage, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Edit contract templates by manually adding content controls

Edit a contract template to reflect any modifications that must be included in the template to generate a standard contract when an employee submits a contract request.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  Open a contract template from the list.

3.  On the form, modify the fields.

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

-   If you edit a contract template in Draft state, it will remain in Draft state.
-   If you edit a contract template in Published state, the state will change to Editing.


</td></tr><tr><td>

Application

</td><td>

Application to which the contract template belongs. This field is automatically set to the application scope in which you’re creating the contract template.

</td></tr><tr><td>

Active

</td><td>

Option to make the template active and available for use.

</td></tr></tbody>
</table>4.  Select **Parse Document** to extract any modified content marked by content control from the imported document.

    -   The existing imported clauses with no change will be retained along with its Classification and Mapping clause.
    -   The imported clauses for which the content controls are deleted in the imported document will be deleted from the list.
    -   Any new added content controls will be listed under Imported clauses, Clause Mapping or Template Mappings.
5.  Classify and map the newly added Imported clauses.

    For more information, see [Classify and map imported clauses](cncore-import-clauses.md).

6.  Select **Update** to save the modifications.

7.  On finalizing the content of the contract document, select **Publish**.


**Parent Topic:**[Manage clauses, tables, and contract templates](../concept/cncore-manage-clauses-ctemplates.md)

**Related topics**  


[Edit a contract clause variation](cncore-edit-cv.md)

[Edit a contract template using Microsoft Word add-in for ServiceNow Contracts](cncore-edit-ct-addin.md)

[Create a contract template from an existing template](cncore-create-template-revision.md)

[Generate and preview a contract document from a template](cncore-preview-template.md)

[Delete a contract template](cncore-delete-template.md)

