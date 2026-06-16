---
title: GRC integration with Thomson Reuters Regulatory Intelligence release notes
description: Version history for the GRC integration with Thomson Reuters Regulatory Intelligence on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-thomson-reuters-regulatory-intel.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC integration with Thomson Reuters Regulatory Intelligence release notes

Version history for the GRC integration with Thomson Reuters Regulatory Intelligence on the ServiceNow Store.

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
        -   Replaced hard-coded admin role dependencies with granular roles, improving security and aligning with least privilege principles.
-   **Version 20.1.1 - May 2025**
    -   New:
        -   Added upgrade scenario changes w.r.t new impacted areas feature.
        -   Implemented demo data changes for the impacted areas feature.
-   **Version 19.0.0 - August 2024**

    Changed: Made demo data changes to improve related documents list view experience.

-   **Version 18.0.0 - February 2024**

    Fixed: Code sign flows for connection validation is fixed.

-   **Version 16.0.0 - May 2023**

    Fixed: Reduction in size of application jar file.

-   **Version 13.0.0 - September 2021**
    -   Changed:
        -   Provider configuration setup has been moved to the taxonomy application.
        -   A single datasource is used to upload the taxonomy data from provider.
        -   Transform map has changed to populate to the new taxonomy tables and classes.
    -   Removed: Table to configure XPATH references of taxonomy XML.
-   **Version 2.0.0 - March 2021**

    New: Initial version of GRC integration with Thomson Reuters Regulatory Intelligence.

-   **Version 1.0.7 - December 2020**

    New: Initial version of GRC integration with Thomson Reuters Regulatory Intelligence.


