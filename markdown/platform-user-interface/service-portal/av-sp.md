---
title: Antivirus Scanning in Service Portal
description: View the health status of file attachments in Service Portal. Antivirus Scanning scans files in the Attachments \[sys\_attachments\] table by default. When viewed from a Service Portal page, attachments may not be available for download depending on their health status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/service-portal/av-sp.html
release: zurich
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Supported features in Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Antivirus Scanning in Service Portal

View the health status of file attachments in Service Portal. Antivirus Scanning scans files in the Attachments \[sys\_attachments\] table by default. When viewed from a Service Portal page, attachments may not be available for download depending on their health status.

**Note:** Antivirus Scanning is a ServiceNow AI Platform feature. For more information, see [Antivirus Scanning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/servicenow-ai-platform-security/antivirus-protection.md).

## Scanning scenarios

Review these scanning scenarios to understand how Antivirus Scanning interacts with attachments in Service Portal.

-   **Upload a file**
    1.  A user uploads an infected file to a record in Service Portal.
    2.  The system scans the file, moves it to quarantine, and displays a message. The file is unavailable for download.

        \[Omitted image "av-sc-page.png"\] Alt text: Message that the file failed the security scan in a Catalog page.

        If viewing the record in the Ticket Form page, the thumbnail does not display.

        \[Omitted image "av-ticket-form-page.png"\] Alt text: Message that the file failed the security scan in the Ticket Form page.

    3.  The system sends an email notification to the user and the antivirus administrator.
-   **Download a file**

    1.  A user opens a record with an attachment in Service Portal.
    2.  The system scans the file and moves it to quarantine. The file is unavailable for download. If viewing the record in the Ticket Form page, the thumbnail does not display.
    3.  The system sends an email notification to the user and the antivirus administrator.
    \[Omitted image "infected-file-form-page.png"\] Alt text: Infected file viewed from a form in the Service Portal.

-   **View a file**
    1.  A user opens a record with an infected attachment.
    2.  The file is unavailable for download. If viewing the record in the Ticket Form page, the thumbnail does not display.

**Parent Topic:**[Supported features in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/service-portal/unsupported-features-sp.md)

