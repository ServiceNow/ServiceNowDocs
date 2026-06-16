---
title: GRC: Advanced Dashboards release notes
description: Version history for the GRC: Advanced Dashboards on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-advanced-dashboards.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Advanced Dashboards release notes

Version history for the GRC: Advanced Dashboards on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACLs include the following enhancements:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
        -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 22.0.1 - March 2026**
    -   Changed:
        -   Prevented the inclusion or update of control objective working drafts in the Entity document and the controls dashboard.
        -   Updated control objective demo data records by setting the record nature field to Current version and the state to Published.
-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   Changed:
        -   The System Administrator role is removed from the Application menu and modules for GRC Advanced Dashboards.
        -   The Control objective field is converted to an optional field on Entity Documents and Controls for the dashboard table.
        -   Updated date population for the Entity document and controls in the dashboard table to take into account direct associations between citations and controls.
-   **Version 20.0.0 - February 2025**

    Fixed: Localisation issues.

-   **Version 18.1.3 - June 2024**

    New: Migrated dashboards to Analytics workspace.

-   **Version 16.0.1 - February 2023**

    Fixed: Access controls for viewing the reports.

-   **Version 15.0.1 - December 2022**

    Fixed: Reduction in the installation size of the application.

-   **Version 15.0.0 - August 2022**

    Changed: Role hierarchy changes: GRC Reader role will not be part of Business User role, modified reports accordingly.

-   **Version 12.0.0 - March 2021**

    Fixed: Enabled License tracking for tables.

-   **Version 10.1.3 - July 2020**
    -   This application provides several persona-based dashboards that can be used with your licensed GRC Policy and Compliance, Risk, and Audit Management applications. The dashboards are available for:

        -   First-line-of-business users such as application owners.
        -   Second-line-of-business users such as risk and compliance users and managers.
        -   Third-line-of-business users such as auditors and audit managers.
    -   The reports help users track daily tasks and approvals, and easily identify new requests. The reports also enable users to be aware of the entire risk and compliance posture of the organization.

