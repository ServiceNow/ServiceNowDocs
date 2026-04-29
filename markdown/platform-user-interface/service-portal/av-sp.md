---
title: Antivirus Scanning in Service Portal
description: View the health status of file attachments in Service Portal. Antivirus Scanning scans files in the Attachments \[sys\_attachments\] table by default. When viewed from a Service Portal page, attachments may not be available for download depending on their health status.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supported features in Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Antivirus Scanning in Service Portal

View the health status of file attachments in Service Portal. Antivirus Scanning scans files in the Attachments \[sys\_attachments\] table by default. When viewed from a Service Portal page, attachments may not be available for download depending on their health status.

**Note:** Antivirus Scanning is a ServiceNow AI Platform feature. For more information, see [Antivirus Scanning](https://www.servicenow.com/docs/access?context=antivirus-protection&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Scanning scenarios

Review these scanning scenarios to understand how Antivirus Scanning interacts with attachments in Service Portal.

-   **Upload a file**
    1.  A user uploads an infected file to a record in Service Portal.
    2.  The system scans the file, moves it to quarantine, and displays a message. The file is unavailable for download.

        ![Message that the file failed the security scan in a Catalog page.](../image/av-sc-page.png)

        If viewing the record in the Ticket Form page, the thumbnail does not display.

        ![Message that the file failed the security scan in the Ticket Form page.](../image/av-ticket-form-page.png)

    3.  The system sends an email notification to the user and the antivirus administrator.
-   **Download a file**

    1.  A user opens a record with an attachment in Service Portal.
    2.  The system scans the file and moves it to quarantine. The file is unavailable for download. If viewing the record in the Ticket Form page, the thumbnail does not display.
    3.  The system sends an email notification to the user and the antivirus administrator.
    ![Infected file viewed from a form in the Service Portal.](../image/infected-file-form-page.png)

-   **View a file**
    1.  A user opens a record with an infected attachment.
    2.  The file is unavailable for download. If viewing the record in the Ticket Form page, the thumbnail does not display.

**Parent Topic:**[Supported features in Service Portal](../reference/unsupported-features-sp.md)

