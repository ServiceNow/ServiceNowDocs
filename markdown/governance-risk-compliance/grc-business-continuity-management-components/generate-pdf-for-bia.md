---
title: Generate BIA reports in PDF or Microsoft Word formats
description: Generate a PDF or Microsoft Word copy of a business impact analysis in the BCM Configurable Workspace and save it for a future reference.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Generate BIA reports in PDF or Microsoft Word formats

Generate a PDF or Microsoft Word copy of a business impact analysis in the BCM Configurable Workspace and save it for a future reference.

## Before you begin

Role required: sn\_bcm.program\_manager, sn\_bcm.planner

## About this task

To format the PDF for your business needs, see [Format PDF templates for BIAs, BCPs, and Events](update-pdf-format-for-bia-bcp-event.md).

Beginning with the Xanadu release, the content in PDFs of Business Impact Analyses, Plans, and Events is improved by implementing a new layout:

-   Arrange the various event tasks in a table format.
-   Include details of the asset owner and the description from the Business Impact Analysis.
-   Display a table that outlines the dependencies of the plan assets.
-   Mark the date of the PDF creation on the front page.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Business Impact Analysis** and select any business impact analysis record that is in the **Review** or next state.

3.  Select **Generate PDF** in the form.

    The example shows the **Generate PDF** option in the business impact analysis form.

    ![Generate the BIA PDF.](../image/bia-pdf-generate-pdf.png)

    The example shows the message that is displayed on the screen: `<Name of the BIA> PDF has been successfully generated for download.`

    ![Downloading the BIA PDF.](../image/bia-pdf-generated-download.png)

4.  To download the PDF, select the link in the message.

    The example shows the PDF of the business impact analysis.

    ![BIA PDF.](../image/bia-pdf-to-be-customized.png)

5.  Save the PDF on your system.

6.  To format the BIA PDF template, follow the instructions in [Format PDF templates for BIAs, BCPs, and Events](update-pdf-format-for-bia-bcp-event.md).

7.  To create the BIA report in Microsoft Word, select **Generate MS Word**

    Generate a report of the BIA record in Microsoft Word format. The Microsoft Word copy of the BIA record is successfully generated that you can download.

8.  To print the BIA report, open the saved PDF or Microsoft Word copy and select **Print**.


**Parent Topic:**[Structured workflows for BIAs](../concept/bia-tasks-performed-by-bia-owner.md)

