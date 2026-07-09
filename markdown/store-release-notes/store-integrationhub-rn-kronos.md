---
title: Kronos spoke release notes
description: Version history for the Integration Hub UKG spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-kronos.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Kronos spoke release notes

Version history for the Integration Hub UKG spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.6.1 - July 2026**
    -   Fixed:
        -   The "Kronos - Refresh The Access Token" flow was failing for Auth0 authentication after 24 hours, preventing tokens from refreshing correctly to maintain the connection.
        -   The Run As field on the trigger auto-script record was mapped to an invalid user in the UKG flows.
-   **Version 3.6.0 - June 2026**
    -   Changed:
        -   Added automatic OAuth token refresh to align with the latest UKG API requirements.
        -   Access control lists \(ACLs\) have been updated to align with current platform security standards.
-   **Version 3.5.0 - December 2025**

    Minor fixes.

-   **Version 1.0.2 - June 2020**
    -   The Kronos Workforce Dimensions spoke provides a list of actions that wraps around the Kronos REST APIs. It provides the foundation to synchronize ServiceNow and Kronos bi-directionally, such as time off request scenario.
        -   Retrieve an employee's accrual time off balance.
        -   Create and update employee time off requests.
        -   View current or historical employee time off requests.

