---
title: GRC: Regulatory Change Management integration with RSS Feeds release notes
description: Version history for the GRC: Regulatory Change Management integration with RSS Feeds on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-rss-feed-integration.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Regulatory Change Management integration with RSS Feeds release notes

Version history for the GRC: Regulatory Change Management integration with RSS Feeds on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACL's
            -   Consistent access control: All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
            -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 21.1.0 - December 2025 \(Zurich\)**
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 20.1.1 - May 2025**

    Changed: Performed demo data corrections with respect to new impacted areas feature on RCM.

-   **Version 19.0.0 - August 2024**

    Changed: Updated the application version to synchronise with dependent application.

-   **Version 18.0.0 - February 2024**

    Fixed code sign flow issue for connection validation.

-   **Version 16.0.0 - February 2023**

    Fixed: Reduction in installation size of the application.

-   **Version 13.0.0 - September 2021**
    -   Changed:
        -   Provider configuration is modified to a new table in GRC: taxonomy management.
        -   RSS feed parser will create default taxonomy values in the new "Regulatory feed to taxonomy mapping" table.
-   **Version 1.0.1 - March 2021**
    -   New:
        -   Support to pull RSS Feeds data
        -   Easy to setup, configurable and robust integration with error handling mechanisms

