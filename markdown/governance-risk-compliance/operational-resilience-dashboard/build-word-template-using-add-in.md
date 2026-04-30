---
title: Build the Word template using the add-in
description: Build the word template using the add-in. The Word Templates module provides the DIR Word templates used to generate Microsoft Word reports.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-16"
reading_time_minutes: 2
breadcrumb: [Generating Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Build the Word template using the add-in

Build the word template using the add-in. The Word Templates module provides the DIR Word templates used to generate Microsoft Word reports.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Digital resilience incident reporting** &gt; **Word Templates**.

2.  To create a Word template, select **New**.

    The Word templates form is displayed.

3.  On the form, fill in the fields.

<table id="table_sgq_pvd_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the Word template for the table that is selected in the **Table** field.

</td></tr><tr><td>

Category

</td><td>

Classification or group to which the Word template belongs.

</td></tr><tr><td>

Table

</td><td>

Table for which the Word template is being created.

</td></tr><tr><td>

Document

</td><td>

Word template that was created based on content configuration.**Note:** The document must be a docx file only. If you attach a document that is in any other format, then an error message appears.

</td></tr><tr><td>

State

</td><td>

State of the Word template record defaults to **Draft**.-   **Draft**: Defaults to Draft state when you open the record.
-   **Published**: State when the Word template is published. You can't update a template when it is in the published state.
-   **Edit**: State in which the record details can be updated.

**Note:** The Word template record in the **Edit** state can’t be used for report generation. The record isn't available to select in the Generate report pop-up.

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

</td></tr><tr><td>

Post processing action

</td><td>

Option to update the generated Word template report with fields from the Report section of the Engagement record.

</td></tr></tbody>
</table>4.  To edit an existing pre-defined template, open the desired Microsoft Word template from the list and select the **Edit** UI action.

5.  Select **OK**.

6.  To delete an existing Word template, select the **Delete** in the record.

7.  To update an existing Word template, complete the following steps.

    1.  Update the name, category, table, or active option of the record.

    2.  To add a brand new document to the Word template, select the **Update** option provided with the Document field.

    3.  Select **Click to add..** in the **Document** field.

    4.  In the Choose an attachment file: dialog box, select **Choose file**, and select **OK**.

    5.  To update an existing document associated with the template, select the **Update** option provided with the Document field.

    6.  Select **Update** in the Word template record.

        The Word template record is updated and the updated template is displayed in the list view.

8.  To publish the Word template, select **Publish** in the record.

    You must publish the Word template before you can use it to generate a Microsoft Word report.


