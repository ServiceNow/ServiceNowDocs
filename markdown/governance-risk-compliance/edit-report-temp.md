---
title: Manage Microsoft Word document templates
description: Manage Microsoft Word document templates centrally using the Admin module in the BCM application. This feature enables you to create or edit templates for BIA, BCP, or other events, providing customized and controlled document generation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/edit-report-temp.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Generating reports using Document designer, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Manage Microsoft Word document templates

Manage Microsoft Word document templates centrally using the Admin module in the BCM application. This feature enables you to create or edit templates for BIA, BCP, or other events, providing customized and controlled document generation.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **General Administration** &gt; **Word templates**.

2.  To create a Microsoft Word template, select **New**.

    Microsoft Word template form is displayed.

    \[Omitted image "word-temp-new-record.png"\] Alt text: Microsoft Word templates form.

3.  On the form, fill in the fields.

    For more information on the fields, see [Word template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/word-template-form.md).

    Microsoft Word templates provided with an instance have two categories: BCM and BIA Smart Assessment.

    \[Omitted image "temp-two-categories.png"\] Alt text: Microsoft Word templates.

    **Note:** Verify that you’re updating Microsoft Word template with the BCM category.

4.  To edit an existing pre-defined template, open the desired Microsoft Word template from the list and select the **Edit** UI action.

    The Edit Microsoft Word template window is displayed with a message: `The templates cannot be used for report generation while in an editing state. Are you sure you want to edit?`

    \[Omitted image "edit-word-temp.png"\] Alt text: Edit a template.

5.  Select **OK**.

6.  To update a Microsoft Word template record, complete these steps.

    1.  Update the name, category, table, or active option of the record.

    2.  To add a document to Microsoft Word template, select the **Update** option provided with the Document field.

    3.  Select **Click to add..** in the **Document** field.

    4.  In the 'Choose an attachment file' dialog box, select **Choose file**, and select **OK**.

    5.  To update an existing document associated with the template, select the **Update** option provided with the Document field.

    6.  Select **Update** in Microsoft Word template record.

        Microsoft Word template record is updated and the updated template is displayed in the list view.

    The process to update a pre-defined template is shown in the example.

    \[Omitted image "update-word-temp.png"\] Alt text: Update the template.

7.  To delete the template, select the **Delete** in the record.

8.  To publish the template, select **Publish** in the record.


