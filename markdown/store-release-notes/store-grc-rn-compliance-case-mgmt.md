---
title: GRC: Compliance Case Management release notes
description: Version history for the GRC Compliance Case Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-compliance-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Compliance Case Management release notes

Version history for the GRC Compliance Case Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New: Manage Smart Assessment templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
    -   Changed: Standardized query range security ACLs are now applied across all tables, ensuring consistent query access for authenticated users with appropriate read permissions throughout the platform. These ACL rules are installed automatically during upgrade with no administrator action required — automated upgrade scripts handle the full transition, including detection and processing of previously customized ACLs to ensure existing configurations continue to function without interruption. If your instance includes administrator-modified query range ACLs, a post-upgrade review is recommended to confirm alignment with your intended access policies.
-   **Version 22.0.1 - March 2026**
    -   New:
        -   Ability to create anonymous compliance cases from the Anonymous Reporting Center portal.
        -   AI-based compliance case summarization capability that covers all the key insights and details of a compliance case.
    -   Fixed: Fixed security bugs.
-   **Version 21.1.0 - December 2025 \(Zurich\)**
    -   New:
        -   Ability to create and map action tasks to the compliance request workflow.
        -   Ability to create dynamic state model for action tasks in compliance requests.
        -   Creation of compliance case from inbound email.
        -   Ability to configure impacted and related areas on compliance case types.
    -   Changed:
        -   Introduced an 'Active' flag in the GRC Choice table. Updates to these flags are now reflected in the AI risk and compliance management application.
        -   Implemented the impacts of Citation-to-Control mapping across the dashboards and overview pages.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 21.0.1 - August 2025**
    -   Changed: Implemented smart assessment changes to compliance case assessments.
    -   Fixed: Fixed issues related to access permissions on compliance case record.
-   **Version 20.2.0 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs on compliance case tables.

-   **Version 20.1.0 - May 2025**
    -   Fixed:
        -   Fixed security directive changes
        -   Fixed coral theme issues related to compliance case feature
        -   Fixed issue on assessment questionnaire and localization issues
-   **Version 20.0.1 - February 2025**
    -   New:
        -   Empower compliance professionals to perform assessments on compliance cases using the Smart Assessment Engine.
        -   Utilize the unified Tasks page on Employee Center to complete your assessments.
    -   Fixed: Localisation and other functional issues are fixed.
-   **Version 19.1.0 - November 2024**

    Changed: Now unit testing framework adoption changes.

-   **Version 19.0.1 - August 2024**
    -   New:
        -   Enable views for Homepage for Compliance analyst persona to manage reported compliance cases or requests.
        -   Set up configurations to auto-calculate the notification dates for reported compliance cases.
    -   Changed: A new graphical chart provisioned for Compliance Case managers to monitor and access compliance cases by subtype classification
-   **Version 18.1.0 - June 2024**

    Changed: Updated this app to the latest version of GRC Case Management Core \(18.1.0\).

-   **Version 18.0.1 - February 2024**
    -   New:
        -   Export "Case/Request" records to PDF
            -   Enables offline sharing of information with stakeholders such as regulators, legal professionals, who may not have access to the application.
            -   Customize multiple PDF templates per case or request types.
        -   Manage Email communication from Case or Requests records
            -   Compliance teams can centrally initiate and monitor all email communications, for various scenarios, such as:
                -   Regulatory inquiries
                -   Regulatory reporting
                -   Legal consultation
    -   Changed:
        -   Updated user experience
            -   Enables to select multiple Impacted and Related areas within a compliance case.
-   **Version 17.0.2 - August 2023**
    -   New: Ability to raise and manage compliance requests.
    -   ServiceNow's Compliance case management solution helps customers manage their compliance cases, such as policy and regulatory violations, complaints, and more. Collaborate with key stakeholders to perform assessments, investigation tasks, and other actions to effectively manage compliance cases. Additionally, analyze the causes and consequences as part of the post-case review process.

