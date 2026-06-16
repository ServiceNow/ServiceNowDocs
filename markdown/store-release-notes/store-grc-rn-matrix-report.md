---
title: Matrix report release notes
description: Version history for the Matrix report application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-matrix-report.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Matrix report release notes

Version history for the Matrix report application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACLs include the following enhancements:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
    -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 21.0.1 - August 2025**

    Fixed: Fixed UI issues and bugs related to Risk details in the Matrix Report.

-   **Version 20.1.1 - May 2025**
    -   Fixed:
        -   Show appropriate information messages when there is no data to display on the report.
        -   Filter conditions when configuring matrix report.
        -   Accessibility changes.
-   **Version 20.0.2 - February 2025**

    The Matrix Report application presents data in a structured grid or table format. You can analyze relationships between different variables, such as assessing risks and controls. The rows in the matrix each represent a specific item, such as a risk, control, or related issue. The columns contain details, such as the name, description, owner, risk ratings, and other data points. For example, an Audit Manager might use a risk and controls matrix report to assess and document risks and internal controls.


