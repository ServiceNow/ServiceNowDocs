---
title: GRC: Privacy Case Management release notes
description: Version history for the GRC: Privacy Case Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-privacy-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Privacy Case Management release notes

Version history for the GRC: Privacy Case Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New: Manage Smart Assessment  templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
    -   Changed:
        -   Query range ACL's
            -   Consistent access control: All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
            -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
        -   Enabled Audit entries support for privacy case and related records.
-   **Version 22.0.1 - March 2026**
    -   New:
        -   Anonymous reporting of privacy cases.
        -   Privacy case summarization capability.
    -   Fixed: Fixed issues related to role mapping and content.
-   **Version 21.1.0 - December 2025 \(Zurich\)**
    -   New:
        -   Introduced the ability to create privacy cases through inbound email.
        -   Added support to configure impacted and related areas based on case type.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles to enhance security and align with least privilege principles.
-   **Version 21.0.1 - August 2025**
    -   Changed: Existing privacy case landing page module is removed and a new tab is added on Privacy landing page to see case management metrics.
    -   Fixed: Fixed demo data issues across the product.
-   **Version 20.2.2 - July 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.2.1 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.0 - May 2025**
    -   Changed:
        -   Fixed coral theming and security issues on privacy case management.
        -   Fixed IO visibility issue on privacy case related list.
        -   Fixed localization issues.
-   **Version 20.0.1 - February 2025**
    -   New: Empower privacy professionals to perform assessments on privacy cases using the Smart Assessment Engine.
    -   Fixed: Fixed issues to improve security of product.
-   **Version 19.1.1 - November 2024**
    -   Fixed:
        -   Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimising zoom capabilities.
        -   Security fixes.
-   **Version 19.0.2 - August 2024**
    -   New:
        -   Collaborate and chat with cross-functional teams for privacy cases and breach assessments.
        -   A new graphical chart enables privacy case managers to monitor and access their privacy cases by the subtype classification.
    -   Changed: Enable your privacy analysts to access a homepage so that your privacy analysts can manage reported privacy cases or requests.
-   **Version 18.1.1 - June 2024**
    -   Changed: Updated the screen &amp; scripted conditions, UX add-on event mappings of declarative actions with Form controller for improved record page performance.
    -   Fixed: Fixed dark theme related issues on modal dialogs.
-   **Version 18.0.2 - February 2024**

    ServiceNow Privacy Case Management helps customers manage their privacy breaches. Collaborate with key stakeholders by performing privacy breach assessments, investigation tasks, and manage and report breach notifications as per regulatory obligations. It also helps to analyze the causes and consequences as part of the post case review process.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

