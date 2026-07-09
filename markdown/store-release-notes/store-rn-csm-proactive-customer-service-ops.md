---
title: Proactive Customer Service Operations release notes
description: Version history for the Proactive Customer Service Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-proactive-customer-service-ops.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Proactive Customer Service Operations release notes

Version history for the Proactive Customer Service Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 25.1.0 - July 2026**
    -   Changed:
        -   Event Management operators now use a dedicated CSM role for access control\(new installations only\)
        -   On new installations, access to Customer Service Management data for Event Management operators is granted through the scoped role sn\_pro\_cs\_ops.csm\_evt\_mgmt\_stakeholder instead of the platform-level evt\_mgmt\_operator role.
        -   Assign sn\_pro\_cs\_ops.csm\_evt\_mgmt\_stakeholder to any Event Management operator who needs visibility into CSM data. The role internally includes evt\_mgmt\_operator, so no additional role assignments are needed. This role grants access to:
            -   Customer service cases — read and add work notes
            -   Install base items — read \(filtered to the operator's account and contacts\)
            -   Customer contacts and account names — read
        -   Existing installations/Upgrades: No action required. Current role assignments and ACL records are unchanged.
-   **Version 25.0.3 - May 2026**
    -   Changed:
        -   Enhanced the performance of "CSM Install Base Outages on Home Page" portal widget
        -   Related API enhancement on the case creation.
-   **Version 25.0.1 - March 2026**

    Changed: Minor enhancements.

-   **Version 24.1.0 - January 2026**

    Changed: Minor enhancements.

-   **Version 24.0.1 - August 2025**

    Minor bug fixes.

-   **Version 24.0.0 - February 2025**

    This version is dependent on the Install base store application and is compatible with the Yokohama release only.

-   **Version 23.1.2 - November 2024**

    Minor security fixes.

-   **Version 23.1.1 - May 2024**
    -   New: Proactive Customer Service Operation now supports i18n localization.
    -   Fixed: Include minor security fixes.
-   **Version 23.0.5 - February 2023**

    The plugin was available as a family plugin until the Tokyo release and as a store app from the Utah release.


