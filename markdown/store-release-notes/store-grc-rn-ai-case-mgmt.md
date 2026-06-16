---
title: AI Case Management release notes
description: Version history for the AI Case Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-ai-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# AI Case Management release notes

Version history for the AI Case Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New: Manage Smart Assessment  templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
    -   Changed: Standardized query range security ACLs are now applied across all tables, ensuring consistent query access for authenticated users with appropriate read permissions throughout the platform. These ACL rules are installed automatically during upgrade with no administrator action required — automated upgrade scripts handle the full transition, including detection and processing of previously customized ACLs to ensure existing configurations continue to function without interruption. If your instance includes administrator-modified query range ACLs, a post-upgrade review is recommended to confirm alignment with your intended access policies.
-   **Version 22.0.1 - March 2026**
    -   New:
        -   New anonymous reporting feature for AI cases.
        -   Support for Managed and unmanaged assets on AI cases and Inquiries.
    -   Changed: Implemented smart assessment template category changes
    -   Fixed: Fixed security and demo data issues.
-   **Version 21.1.1 - December 2025 \(Zurich\)**

    New: The new inbound email feature allows users to create AI cases and inquiries directly from email, enabling a simple and streamlined case creation experience for employees.

-   **Version 21.0.1 - August 2025**
    -   New:
        -   Use AI cases tab to monitor and manage AI case activity
            -   Access the AI cases tab in the AI Risk and Compliance workspace to gain a centralized overview of all AI assets cases and inquiries. This tab presents a structured list of records that include case details such as status, priority, owner, and timeline, enabling you to monitor their progression efﬁciently. Use this view to stay informed about ongoing investigations, follow up on pending actions, and ensure timely resolution of AI asset's issues. The tab also supports ﬁltering and sorting options, helping you prioritize cases that require immediate attention and streamline case management processes.
-   **Version 20.2.0 - June 2025**

    Fixed: Added query-range ACLs for AI Case table.

-   **Version 20.1.3 - May 2025**

    AI Case management to oversee AI asset-related inquiries and cases, enabling faster response and improved tracking.


