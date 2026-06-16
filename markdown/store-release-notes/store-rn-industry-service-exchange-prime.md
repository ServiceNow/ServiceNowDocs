---
title: Service Exchange - Prime release notes
description: Version history for the ServiceNow Service Exchange - Prime application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-industry-service-exchange-prime.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Public Sector Industry release notes, ServiceNow Store release notes]
---

# Service Exchange - Prime release notes

Version history for the ServiceNow® Service Exchange - Prime application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.0.2 - June 2026**
    -   Connections tab in the Service Exchange Center: Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.
    -   Improved consumer registration and onboarding: Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.
    -   Improved FDS capabilities:
        -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
        -   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
        -   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
        -   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.
    -   Journal Field Framework enhancements
        -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
        -   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting
    -   Group-based persona assignments for Remote Catalog: Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.
-   **Version 1.0.1 - April 2026**

    Service Exchange Onboarding introduces AI Agents that streamline the initiation of the registration process by automating the creation of Consumer Registration tasks, monitoring for issues, and guiding administrators through remediation if any are found. This reduces manual effort, improves accuracy, and enhances the onboarding experience.


**Parent Topic:**[ServiceNow Store - Public Sector Industry release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-public-sector-highlight.md)

