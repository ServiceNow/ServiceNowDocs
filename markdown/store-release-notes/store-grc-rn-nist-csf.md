---
title: GRC: NIST CSF Use Case Accelerator release notes
description: Version history for the GRC: NIST CSF Use Case Accelerator Use Case Accelerator on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-nist-csf.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: NIST CSF Use Case Accelerator release notes

Version history for the GRC: NIST CSF Use Case Accelerator Use Case Accelerator on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACLs include the following enhancements:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
    -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 22.0.1 - March 2026**
    -   Changed:
        -   Allow business workflow on control objective current version records only
        -   Prevent association of control objectives which are working drafts to NIST CSF activity objects in the Gap table
        -   Updated control objective content records with record nature field as Current version and state as published
-   **Version 21.1.0 - December 2025 \(Zurich\)**

    New: GRC choices used for the NIST CSF Use Case Accelerator can be activated or deactivated with the new Active field.

-   **Version 20.1.1 - May 2025**

    Fixed: Control provider role was able to create and update Orient targets.

-   **Version 20.0.0 - February 2025**
    -   Fixed:
        -   Localization issues
        -   More than one Target without entity
-   **Version 19.0.1 - August 2024**

    New: Added NIST CSF 2.0 content - authority document, citations, policies, and control objectives.

-   **Version 18.1.0 - June 2024**

    New: Migrated dashboards to Analytics workspace.

-   **Version 18.0.1 - February 2024**

    Fixed: On the risk statements, source is showing incorrect value.

-   **Version 17.0.0 - August 2023**

    Fixed: Cleaned up auto generated business rules as the functionality is already handled.

-   **Version 16.0.2 - February 2023**
    -   Fixed:
        -   Enabled license tracking for Risk executive, Security officer, User, and Control provider roles.
        -   Access controls for viewing reports.
        -   Reduction in installation size of the application.
-   **Version 14.1.3 - March 2022**

    Changed: Support for multiple controls

-   **Version 11.0.0 - October 2020**

    Changed: Enabled report\_view\_acl by default

-   **Version 10.1.0 - June 2020**

    Changed: The internal plugin name has been changed

-   **Version 9.0.1 - November 2019**

    This application was released for the Madrid family release and is still compatible with New York.

-   **Version 7.0.1 - May 2019**

    Initial release to the ServiceNow Store.


