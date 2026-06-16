---
title: Cloud Services Catalog release notes
description: Version history for the Cloud Services Catalog application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cloud-services-catalog.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - ITOM Cloud Accelerate release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Cloud Services Catalog release notes

Version history for the Cloud Services Catalog application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.6.0 - June 2026**
    -   Fixed:
        -   UI issues in the User Portal and Employee Portal affecting WCAG compliance
        -   Start and Stop operations at the stack and resource level not translating correctly per i18n standards
        -   VoiceOver and Tab control accessibility issues across the My Stacks, My Resources, and My Requests pages
        -   Tabs on the Stack detail page incorrectly announced as selected by screen readers
        -   My Stacks page showing no data after enabling AI Search in the Employee Portal
        -   Spurious query range error appearing on the Incident page for cloud service users
        -   Manage access through predefined query access controls for all Cloud Service Catalog tables
-   **Version 1.5.1 - December 2025**
    -   New:
        -   Introduced granular, feature-specific admin roles to replace the broad 'admin' role, significantly improving security by minimizing excess access. These new roles are seamlessly integrated into the standard administrative experience.​
        -   Introduced GitHub Actions integration with Cloud Services Catalog, enabling automated discovery and execution of GitHub Actions workflows from the ServiceNow instance to manage provisioned resources.
    -   Fixed: Implemented Read-Only Field Remediation by introducing a new ChoiceList, 'read\_only\_option,' to replace the previous 'read\_only' field \(which was prone to unauthorized client-side updates\). This change prevents client-side manipulation of read-only fields and significantly mitigates security risks across all applications.
-   **Version 1.4.1 - July 2025**
    -   Fixed:
        -   Resolved the issue where a "workflow or flow required" banner is incorrectly displayed even after a flow was assigned during new catalog item creation
        -   The CSC Resource details page now loads correctly with discovered resources accessed from "My Resources"
-   **Version 1.4.0 - May 2025**

    New: Support for Coral theme added.

-   **Version 1.3.7 - November 2024**

    No updates.

-   **Version 1.3.6 - May 2024**
    -   New:
        -   Link from CSC \(employee centre\) to Tag dashboard
        -   Link from CSC \(employee centre\) to Cloud Admin Portal
        -   Support for integration with Tofu Open-source \(Version 1.6.x onwards\). Please refer to the documentation for implementation details.
-   **Version 1.3.0 - November 2023**

    Spur your organization's cloud adoption through governed workflows for cloud automation with Cloud Services Catalog \(CSC\). Be it for IaaS or PaaS needs, or even setting up an environment with a development or production stack you can drive the workflow automation using CSC.


