---
title: Build the Microsoft Word template using the add-in
description: Build the Microsoft Word template using the add-in. The Word Templates module provides the Digital resilience incident \(DRI\) Word templates that are used to generate Microsoft Word reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/build-word-template-using-add-in.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Generating Microsoft Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Build the Microsoft Word template using the add-in

Build the Microsoft Word template using the add-in. The Word Templates module provides the Digital resilience incident \(DRI\) Word templates that are used to generate Microsoft Word reports.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager

## About this task

Before building a Microsoft Word template, sign in to your instance from the Word add-in with your credentials.

\[Omitted image "document-designer-sign-in-dialog.png"\] Alt text: Document designer sign-in dialog.

## Procedure

1.  Navigate to **All** &gt; **Digital resilience incident reporting** &gt; **Word Templates**.

2.  To create a Microsoft Word template, select **New**.

    The Microsoft Word templates form is displayed.

3.  On the form, fill in the fields.

<table id="table_sgq_pvd_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the Microsoft Word template for the table that is selected in the **Table** field.

</td></tr><tr><td>

Category

</td><td>

Classification or group to which the Microsoft Word template belongs.

</td></tr><tr><td>

Table

</td><td>

Table for which the Microsoft Word template is being created.

</td></tr><tr><td>

Document

</td><td>

Microsoft Word template that was created based on content configuration.**Note:** The document must be a docx file only. If you attach a document that is in any other format, then an error message appears.

</td></tr><tr><td>

State

</td><td>

State of the Microsoft Word template record defaults to **Draft**.-   **Draft**: Defaults to Draft state when you open the record.
-   **Published**: State when the Microsoft Word template is published. You can't update a template when it is in the published state.
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

Option to update the generated Microsoft Word template report with fields from the Report section of the Engagement record.

</td></tr></tbody>
</table>    State transitions for Microsoft Word template are listed:

    -   **Draft** \(initial\)
    -   **Edit** \(record can be modified; not usable for report generation\)
    -   **Published** \(active and selectable in the Generate report dialog\).
4.  To insert a Microsoft 365 reporting item into the template, select the Add Content icon in the ServiceNow ribbon group of Microsoft Word.

    Key features of the ServiceNow ribbon in Microsoft Word are listed:

    -   Design Template — Inserts empty data points that populate when a document is generated.
    -   Add Content — Inserts live data \(reports, charts, visualizations\) into the document directly.
    -   Manage Content — Lists all content inserted via Add Content, with hyperlinks to navigate to specific content blocks and back to the reporting configuration in ServiceNow.
    The panel offers the following report types: **Data point**, **Table**, and **Charts** \(bar chart and pie chart\).

    \[Omitted image "document-designer-add-in-panel-tabs.png"\] Alt text: Document designer add-in panel tabs.

    **Note:** The reporting items that appear in the panel are obtained from the records you created in the Reporting Configurations module. For information, see [Create reporting configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reporting-configurations.md).

5.  Select a reporting item and select **Add** to insert the item at the cursor position in the Word document.

6.  To edit an existing pre-defined template, open it from the list, select **Edit**, update the details, and select **OK**.

7.  To delete an existing template, select **Delete** in the record.

8.  To publish the template, select **Publish** in the record.

    You must publish a template before using it to generate a Microsoft Word report.


**Related topics**  


[Generate a Microsoft Word report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/generate-word-report.md)

