---
title: Generate reports for BIAs, BCPs, and events
description: Generate customized reports for BIAs, BCPs, and events directly from their respective records in Microsoft Word format. This functionality enables you to streamline reporting of impact analyses, plans, and events within your organization.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generating reports using Document designer, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Generate reports for BIAs, BCPs, and events

Generate customized reports for BIAs, BCPs, and events directly from their respective records in Microsoft Word format. This functionality enables you to streamline reporting of impact analyses, plans, and events within your organization.

## Before you begin

Role required: sn\_bcm.manager and sn\_grc\_doc\_design.reader

## About this task

You can control whether to retain or replace the existing report attachments by configuring the **sn\_bcm.retain\_report\_attachments** system property.

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Open a BIA, BCP, or event record from the list view.

3.  To generate a report of the record in Microsoft Word format, select **More \(...\)** and then choose **Generate MS Word** in the record view.

    A BIA record with the UI action is shown in the example.

    ![BIA record.](../image/gen-ms-word-action.png)

    The Generate report window is displayed.

    ![Generate report window.](../image/generate-report.png)

4.  Select the report template for the BIA, BCP, or event and add the name of the report.

5.  Select **Generate**.

    A message is displayed on the screen: `Report is being generated. Refresh the record shortly to view the updates.`

6.  Navigate to the **Details** tab of the record and view the report listed in the Activity section.

    The report is generated in Microsoft Word format and it’s displayed in the Activity section of the record.

7.  Download the report in your ServiceNow instance or in the cloud \(Microsoft Office 365\).

    You can save the generated reports of the BIAs, BCP, and events in your ServiceNow instances or in Microsoft Office 365 for future references.


