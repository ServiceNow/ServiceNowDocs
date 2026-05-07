---
title: Generate event reports in PDF or Microsoft Word
description: Generate the PDF or Microsoft Word copy of an exercise or a crisis event in the BCM Configurable Workspace and save it for a future reference.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Generate event reports in PDF or Microsoft Word

Generate the PDF or Microsoft Word copy of an exercise or a crisis event in the BCM Configurable Workspace and save it for a future reference.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

To format the PDF for your business needs, see [Format PDF templates for BIAs, BCPs, and Events](update-pdf-format-for-bia-bcp-event.md).

Beginning with the Xanadu release, the content in PDFs of Business Impact Analyses, Plans, and Events is improved by implementing a new layout:

-   Arrange the various event tasks in a table format.
-   Include details of the asset owner and the description from the Business Impact Analysis.
-   Display a table that outlines the dependencies of the plan assets.
-   Mark the date of the PDF creation on the front page.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises**.

2.  Select any event record that is in the **Review** or next state from the list view.

    You can use the same process of generating the PDF for a crisis event.

3.  Select **Generate PDF** in the form.

    The example shows the message that is displayed on the screen: `<Name of the exercise event> PDF has been successfully generated for download.`

    ![Downloading the event PDF.](../image/event-pdf-download.png)

4.  To download the PDF, select the link in the message.

    The example shows that the PDF of the exercise has been downloaded locally.

    ![Event PDF that can be customized.](../image/event-pdf-to-be-customized.png)![Event details.](../image/event-details-pdf.png)

5.  Save the PDF on your system.

    You can save the PDF for a future reference.

6.  To format the Events PDF template, follow the instructions in [Format PDF templates for BIAs, BCPs, and Events](update-pdf-format-for-bia-bcp-event.md).

7.  To create the event report in Microsoft Word, select **Generate MS Word**.

    Generate a report of the event or crisis record in Microsoft Word format. The Microsoft Word copy of the BIA record is successfully generated that you can download.

    For more information on generating reports in Microsoft Word format using Document designer, see [Generating reports using Document designer](../concept/integrating-document-designer-with-bcm.md).

8.  To print the report, open the saved PDF or Microsoft Word copy and select **Print**.


**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)

