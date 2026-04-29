---
title: Deploy Microsoft Outlook Add-In for Legal Service Delivery
description: Deploy Microsoft Outlook Add-In for Legal Service Delivery for it to be available in Microsoft Outlook to submit legal requests.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Outlook Add-In for Legal Service Delivery, Microsoft Outlook Add-In for Legal Service Delivery, Integration with Third-party applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Deploy Microsoft Outlook Add-In for Legal Service Delivery

Deploy Microsoft Outlook Add-In for Legal Service Delivery for it to be available in Microsoft Outlook to submit legal requests.

## Before you begin

Role required: sn\_lg\_ops.request\_fulfiller

## Procedure

1.  Open Microsoft Outlook.

2.  On the Outlook ribbon, click **Get Add-ins**.

3.  Select **My add-ins**.

4.  In the Custom add-ins section, select **Add a custom add-in** &gt; **Add from file**.

5.  Select the manifest file that you have downloaded.

6.  Select **Install**.


## Result

The ServiceNow for Legal Add-in is available in the Outlook ribbon.

If you do not want to open the ServiceNow for Legal add-in each time you select a new email, keep it pinned by making changes to the manifest file. For more information on the changes to be made to the manifest file, see [Implement a pinnable task pane in Outlook](https://learn.microsoft.com/en-us/office/dev/add-ins/outlook/pinnable-taskpane?tabs=jsonmanifest) topic in the Microsoft Outlook documentation.

**Parent Topic:**[Configure Microsoft Outlook Add-In for Legal Service Delivery](../concept/lsd-outlook-addin-configure.md)

