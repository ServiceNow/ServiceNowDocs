---
title: GRC: Policy and Compliance integrator release notes
description: Version history for the GRC: Policy and Compliance integrator application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-policy-compliance-integrator.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Policy and Compliance integrator release notes

Version history for the GRC: Policy and Compliance integrator application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACLs include the following enhancements:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
        -   Post-upgrade review for customized ACLs:
            -   If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 22.0.1 - March 2026**

    Changed: Prevent association of working draft control objectives with other objects in the "Control objective to object staging" table.

-   **Version 21.1.0 - December 2025 \(Zurich\)**

    Fixed issues: Added read-only attribute to read-only table fields for enhanced security.

-   **Version 19.1.1 - November 2024**

    Fixed: Security fix.

-   **Version 16.0.2 - May 2023**
    -   New:
        -   Staging table to ship mappings between control objectives and configuration tests.
        -   Processing logic to move staging table mappings to actual tables.
-   **Version 16.0.1 - February 2023**

    Fixed: Reduction in installation size of the application.

-   **Version 14.1.2 - March 2022**

    GRC: integrations with third-party content provides a common framework for content providers to push their content like authority documents, citations, control objectives, and additional content types.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

