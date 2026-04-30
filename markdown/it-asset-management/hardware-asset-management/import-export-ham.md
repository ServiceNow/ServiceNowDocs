---
title: Import and export content data
description: Import and export content data to the ServiceNow Hardware Asset Management content service to improve the normalization process. On-premise users can use the Manage Hardware Library module to import or export data via a zip file.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Work with hardware normalization, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Import and export content data

Import and export content data to the ServiceNow Hardware Asset Management content service to improve the normalization process. On-premise users can use the Manage Hardware Library module to import or export data via a zip file.

## Before you begin

Role required:

-   ham\_admin
-   domain\_admin \(if domain separation is enabled\)

## Procedure

1.  Navigate to **Modules** and search for **Manage Hardware Library**.

2.  Open the Manage Hardware library form layout and select the **Active** check box to activate the module.

3.  Click **Save** and refresh the form layout.

4.  Navigate to the Manage Hardware Library module.

5.  Import the content data to get the new data into your system.

    1.  Click **Import Hardware Library Content**.

    2.  Click **Attach Content File** and then select the zip file that contains the content.

    3.  Click **Run Import**.

        After the data is imported, the content update schedule job, **HAM - Apply latest content changes**, is triggered to process the content updates.

6.  Export content to send the custom data or any hardware models that are not fully normalized to the ServiceNow content service team.

    1.  Click **Content Service Opt-in: Export Hardware Normalization Content**.

    2.  If you already haven't opted in to share the data with ServiceNow content service, click **opt-in** and refresh the Manage Hardware Library page.

    3.  Click **Run Export**.

    4.  After the status changes to Ready for Download, refresh the page.

        A zip file is created and appears at the top of the Manage Hardware Library page. If there is no content to export, an error message appears informing you that no content exists.

    5.  Download and send this zip file to the ServiceNow content service team.


**Parent Topic:**[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

