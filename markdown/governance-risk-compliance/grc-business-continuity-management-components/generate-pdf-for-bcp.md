---
title: Generate BCP reports in PDF or Microsoft Word format
description: Generate a PDF or Microsoft Word copy of a business continuity plan in the BCM Configurable Workspace and save it for a future reference.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Generate BCP reports in PDF or Microsoft Word format

Generate a PDF or Microsoft Word copy of a business continuity plan in the BCM Configurable Workspace and save it for a future reference.

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

2.  In the List view, navigate to **Planning** and select any business continuity plan record that is in the **Review** or next state.

3.  Select **Generate PDF** in the form.

    The example shows the message that is displayed on the screen: `<Name of the BCP> PDF has been successfully generated for download.`

    ![Generating the BCP PDF.](../image/bcp-pdf-generated.png)

4.  To format the BCP PDF template, follow the instructions in [Format PDF templates for BIAs, BCPs, and Events](update-pdf-format-for-bia-bcp-event.md).

5.  To download the PDF, select the link in the message and open the PDF.

    The example shows the PDF of a business continuity plan.

    ![BCP PDF.](../image/bcp-pdf-for-modification.png)

6.  Save the PDF on your system.

    You can save the PDF for a future reference.

7.  To create the BCP report in Microsoft Word, select **Generate MS Word**

    Generate a report of the BCP record in Microsoft Word format. The Microsoft Word copy of the BIA record is successfully generated that you can download.

8.  To print the BCP report, open the saved PDF or Microsoft Word copy and select **Print**.


**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

