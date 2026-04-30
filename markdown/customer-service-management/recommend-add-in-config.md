---
title: Include a combined CSM and ITSM add-in icon in Microsoft Outlook
description: Enable users to access both CSM and ITSM through one combined add-in icon.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating with Microsoft Outlook, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Include a combined CSM and ITSM add-in icon in Microsoft Outlook

Enable users to access both CSM and ITSM through one combined add-in icon.

## Before you begin

Role required: sn\_customerservice.contact\_manager and sn\_customerservice.proxy\_contact

## Procedure

1.  Go to your ServiceNow instance.

2.  Navigate to **ServiceNow Add-Ins for Office** &gt; **Office Add-in Manifests**.

3.  Download the manifest files for CSM and ITSM.

    |Option|Description|
    |------|-----------|
    |**ServiceNow for CSM**|Manifest file for CSM.|
    |**ServiceNow for ITSM**|Manifest file for ITSM.|

4.  Click **Download Manifest**.

5.  Install the ServiceNow Add-in for Microsoft Outlook add-in.

    Follow the procedure in [Install the ServiceNow Add-in for Microsoft Outlook](install-servicenow-outlook.md).

    The ServiceNow for CSM/ITSM icon appears in the header and users can view both the CSM and ITSM tasks through it. ![The ServiceNow for CSM/ITSM add-in icon to create incidents, VTB tasks, or contacts.](../image/outlook-itsm-csm-tasks.png)


