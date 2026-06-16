---
title: Microsoft Teams Chat Connector for Security Incident Management release notes
description: Version history for the Microsoft Teams Chat Connector for Security Incident Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-ms-teams-chat-connector.html
release: store
topic_type: reference
last_updated: "2025-10-16"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Microsoft Teams Chat Connector for Security Incident Management release notes

Version history for the Microsoft Teams Chat Connector for Security Incident Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.30 - October 2025**

    Fixed failure in bulk user creation process in Teams to ensure all users are added successfully.

-   **Version 1.2.20 - August 2025**
    -   Fixed:
        -   Enhanced the logic for adding members to Teams and Channels by introducing graceful handling of HTTP 429 \(Too Many Requests\) errors. This includes retry mechanisms with backoff to respect Microsoft Graph API throttling limits and prevent abrupt failures during bulk user operations.
        -   Implemented robust error handling for HTTP 503 \(Service Unavailable\) errors across Microsoft Teams actions. The system now includes automated retries and clearer logging to maintain stability during temporary Microsoft service disruptions.
-   **Version 1.2.12 - November 2024**

    Fixed: Resolved an issue where a 401 error occurred while attempting to obtain an OAuth token when Teams were configured in MSIM, ensuring successful authentication.

-   **Version 1.2.11 - May 2024**
    -   Changed:
        -   Add user groups from MSIs to provide access to the Microsoft Teams channels
        -   Rename the team and post a task activity in the channels
-   **Version 1.2.7 - March 2024**

    Changed: Added a navigation link to Microsoft Teams on the chat channel modal of the workspace.

-   **Version 1.2.6 - February 2024**

    Fixed: Microsoft Teams notifications issue.

-   **Version 1.2.5 - August 2023**

    Fixed: Updated the Spoke application dependency.

-   **Version 1.2.4 - February 2023**

    Changed: Updated to support certificate-based authentication.

-   **Version 1.2.0 - March 2022**

    Fixed: Bug fixes.

-   **Version 1.1.0 - December 2021**

    Allows you to track teams chat activities using Microsoft Teams Collaboration component.


