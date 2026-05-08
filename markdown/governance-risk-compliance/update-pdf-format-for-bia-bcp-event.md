---
title: Format PDF templates for BIAs, BCPs, and Events
description: Format the PDF templates that are used for generating the PDFs of business impact analyses, business continuity plans, or events. You can format the PDFs according to your organizational requirements and templates.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Format PDF templates for BIAs, BCPs, and Events

Format the PDF templates that are used for generating the PDFs of business impact analyses, business continuity plans, or events. You can format the PDFs according to your organizational requirements and templates.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.planner, sn\_bcm.program\_manager

The BCM admin role \(sn\_bcm.admin\) inherits Document Templates roles \(sn\_doc.reader and sn\_doc.writer\) through the sn\_bcm.core\_manager role, rather than containing them directly. These inherited roles enable BCM administrators to create, read, and write Document Templates \(sn\_doc\_template\). BCM products use the Document Templates application to generate and print PDFs. As a result, BCM administrators can edit the content of PDFs within BCM document templates.

![PDF.](../image/edit-pdf-bcm.png)

Verify that you have downloaded the PDF of a business impact analysis, business continuity plan, or event according to the steps mentioned in these topics:

-   [Generate BIA reports in PDF or Microsoft Word formats](generate-pdf-for-bia.md)
-   [Generate BCP reports in PDF or Microsoft Word format](generate-pdf-for-bcp.md)
-   [Generate event reports in PDF or Microsoft Word](generate-pdf-for-events.md)

## About this task

Beginning with the Xanadu release, the content in PDFs of Business Impact Analyses, Plans, and Events is improved by implementing a new layout:

-   Arrange the various event tasks in a table format.
-   Include details of the asset owner and the description from the Business Impact Analysis.
-   Display a table that outlines the dependencies of the plan assets.
-   Mark the date of the PDF creation on the front page.

## Procedure

1.  Navigate to **Document Templates** &gt; **All Document Templates** in the Business Continuity Workspace.

    The document templates for BCM are displayed as shown in the example.

    ![Document templates for BCM.](../image/document-templates-bcm.png)

2.  To update the BIA template, select it from the list view and select **Edit**.

    **Note:** To edit the PDF, save it to your local drive first, and then make your edits.

    The BIA template is shown in the example.

    ![BIA template.](../image/bia-pdf-template.png)

    1.  Select the desired UI action, update the template, and save the changes.

        The PDF template can be updated according to your requirements.

        You can use the same process to update the PDF of a business impact analysis, business continuity plan, exercise, or crisis event.

        **Note:**

        With the BCM administrator \(sn\_bcm.admin\) role, you can navigate to **All Document Templates** in an instance to view the document templates that are provided with the BCM application.

        You can also use an editable and fillable PDF template to format the PDF. For more information on the PDF document template that can be used to customize your PDFs, see [Configure a PDF document template](https://www.servicenow.com/docs/access?context=configure-editable-pdf&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

3.  To insert date variables in the PDF, select **Insert Date**.

    You can use the button multiple times to add different types of dates based on the variables you choose.

4.  To insert the table of contents in the PDF, select **Insert Table of Contents**.

5.  To add blocks for advanced search, select **Add Blocks**.

<table id="choicetable_ib1_wzc_tcc"><tbody><tr><td id="d389483e247">

**To add an existing document block to the template**

</td><td>

In Search blocks, type in the name of an existing document block, select the document block, and select **Insert**.

</td></tr><tr><td id="d389483e259">

**To add a new document block to the template**

</td><td>

Select **Create New Block**.

</td></tr></tbody>
</table>6.  To publish the template, select **Publish**.

    Confirm that the template is published so that the PDF is generated with the right attributes.

    For more information on Document Templates, see [Configure a PDF document template](https://www.servicenow.com/docs/access?context=configure-editable-pdf&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

7.  To copy an existing template, select it from the list and select **Copy**.

8.  To update an existing template, select it from the list and select **Preview**.

9.  To update an existing template, select it from the list and select **Update**.

10. To update the BCP template, select it from the list view and select **Edit**.

    The BCP template is shown in the example.

    ![BCP template.](../image/bcp-pdf-template.png)

    1.  Select the desired UI action, update the template, and save the changes.

        You can update the title of the PDF and the fonts according to your organizational templates.

11. To update the Events template, select it from the list view and select **Edit**.

    The Events template is shown in the example.

    ![Events template.](../image/event-pdf-template.png)

    1.  Select the desired UI action, update the template, and save the changes.

        You can save the PDF for future reference.

12. To add a company logo to the PDF, use a PDF editor like Adobe Acrobat Pro to insert the logo, or insert it into the source document before exporting it as a PDF.

13. To print the report, open the saved PDF or Microsoft Word copy and select **Print**.


