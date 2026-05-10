---
title: Word template form
description: The table gives a description of the field values for the Word template form.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a Microsoft Word template record for an audit report, Generate an audit report for an engagement using Microsoft Word template, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Word template form

The table gives a description of the field values for the Word template form.

<table id="table_sgq_pvd_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the Word template for the table that is selected in the Table field.

</td></tr><tr><td>

Category

</td><td>

Classification or group to which the Word template belongs.For example, Audit for audit-related Word template.

To create a Word template category, see [Word template category form](audit-word-template-category.md).

</td></tr><tr><td>

Table

</td><td>

Record table for which the Word template is being created.

</td></tr><tr><td>

Document

</td><td>

Word template that was created based on content configuration.**Note:** The document must be a docx file only. If you attach a document that is in any other format, then an error message appears.

</td></tr><tr><td>

State

</td><td>

State of the Word template record defaults to Draft.-   Draft: Defaults to Draft state when you open the record.
-   Published: When the Word template record is published. You can't update the record in the published state.
-   Edit: State in which the record details can be updated.

**Note:** The Word template record in Edit state can’t be used for report generation. The record isn't available to select in the Generate report pop-up. See [Generate a report for an engagement in a classic report template](../../grc-workspace-audit/task/generate-report-engagement-audit-ws.md).


</td></tr><tr><td>

Active

</td><td>

Option to activate the record.

</td></tr><tr><td class="sub-head" colspan="2">

Word document generation configurations

</td></tr><tr><td>

Cloud enabled

</td><td>

Option to manage the generated report either as a sys\_attachment in the engagement record or as a cloud document.You can access the document in the cloud either from the Microsoft SharePoint or Google Drive site based on your cloud upload configuration.

For more information, see [Manage your documents and work papers with Audit Management as cloud files](../concept/manage-cloud-docs-using-onedrive-int.md).

</td></tr><tr><td>

Post processing action

</td><td>

Option to update the generated Word template report with fields from the Report section of the Engagement record.Options are:

-   **Populate audit word template and report fields**: If you choose Word report-based template, the fields from the Report section of the Engagement record populate in the Word report.

**Note:** This option is available only if Audit Management application is installed.

-   **None**: Report is generated as a sys attachment or a cloud file. However, no post processing action happens to add or update any report-based fields of the engagement record to the Word report that is generated.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring ATO artifacts report templates](../../grc-cam/reference/cam-configure-word-based-template.md)

