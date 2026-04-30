---
title: Word template form
description: Use Microsoft Word template form to add details about Microsoft Word template for creating reports in the Business Continuity Workspace.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage Microsoft Word document templates, Generating reports using Document designer, Business Continuity Management, Governance, Risk, and Compliance]
---

# Word template form

Use Microsoft Word template form to add details about Microsoft Word template for creating reports in the Business Continuity Workspace.

## Microsoft Word template form

<table id="table_sgq_pvd_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of Microsoft Word template for the table that is selected in the **Table** field.

</td></tr><tr><td>

Category

</td><td>

Classification or group to which the template belongs.For example, BCM for BCM-related Microsoft Word template.

</td></tr><tr><td>

Table

</td><td>

Table for which Microsoft Word template is being created.

</td></tr><tr><td>

Document

</td><td>

Microsoft Word template that was created based on content configuration, for example, BIA template.docx or Plan template.docx.**Note:** The document must be a docx file only. If you attach a document that is in any other format, then an error message appears.

</td></tr><tr><td>

State

</td><td>

State of Microsoft Word template record defaults to **Draft**.-   **Draft**: Defaults to the Draft state when you open the record.
-   **Published**: Microsoft Word template record is published. You can't update the record in the published state.
-   **Edit**: State in which the record details can be updated.

**Note:** Microsoft Word template record in the **Edit** state can’t be used for report generation. The record isn't available to select in the Generate report pop-up.


</td></tr><tr><td>

Active

</td><td>

Option to activate the record.

</td></tr><tr><td class="sub-head" colspan="2">

Word document generation configurations

</td></tr><tr><td>

Cloud enabled

</td><td>

Option to manage the generated report either as a sys\_attachment in the engagement record or as a cloud document.You can access the document either from the Microsoft SharePoint or Google Drive site based on your cloud upload configuration.

</td></tr><tr><td>

Post processing action

</td><td>

Option to update the generatedMicrosoft Word template report with fields from the Report section of the Engagement record.Options are:

-   **Populate BIA word template and report fields**: When you choose this template, the fields from the Report section of the BIA record populate in Microsoft Word report.
-   **Populate BCP Plan word template and report fields**: When you choose this template, the fields from the Report section of the BCP plan record populate in Microsoft Word report.
-   **Populate Recovery Event word template and report fields**: When you choose this template, the fields from the Report section of the Recovery Event record populate in Microsoft Word report.
-   **None**: Report is generated as a sys attachment or a cloud file. However, no post processing action happens to add or update any report-based fields of the record to Microsoft Word report that is generated.

</td></tr></tbody>
</table>