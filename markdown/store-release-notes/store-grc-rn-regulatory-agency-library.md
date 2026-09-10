---
title: Regulatory Agency Library release notes
description: Version history for the Regulatory Agency Library application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-regulatory-agency-library.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance version history release notes, ServiceNow Store version history release notes]
---

# Regulatory Agency Library release notes

Version history for the Regulatory Agency Library application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 23.0.2 - September 2026 \(Brazil\)**
    -   New:
        -   Improved protection against unauthorised query-based data discovery.
        -   ACL behaviour across new installs, upgrades, and true-up releases.
        -   Reduced operational dependency on manual remediation activities.
        -   Zurich and Australia compatibility maintained for supported store applications.
-   **Version 22.5.1 - August 2026 \(Australia\)**

    Changed: As part of MRA Security Enhancements, strengthened authorization validation in Multiple Record Association \(MRA\) workflows to ensure consistent access checks during record association operations.

-   **Version 21.1.6 - August 2026 \(Zurich\)**

    Changed: As part of MRA Security Enhancements, strengthened authorization validation in Multiple Record Association \(MRA\) workflows to ensure consistent access checks during record association operations.

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   Changed:
        -   Query range ACL's
            -   Consistent access control: All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
            -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New: Ability to map assessment templates at regulatory agency profile record and automate the assessment creation for cases based on the agency mapping.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 21.0.0 - August 2025**

    Fixed: Fixed issue related to dependency management.

-   **Version 20.1.0 - May 2025**

    Fixed: Localisation issues are fixed.

-   **Version 20.0.1 - February 2025**
    -   New: Added new widget to Regulatory agency overview page to monitor email activities or statistics.
    -   Fixed: Fixed localisation issue.
-   **Version 19.1.1 - November 2024**
    -   Fixed:
        -   Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimising zoom capabilities.
        -   Security fixes.
-   **Version 19.0.1 - August 2024**

    Establish and maintain a centralized library of regulatory agencies and key contacts. Consolidate and organize regulatory communications via email for future reference as part of the agency records.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

