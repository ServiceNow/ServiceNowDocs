---
title: GRC: Technology Controls Monitoring Accelerator release notes
description: Version history for the GRC: Technology Controls Monitoring Accelerator on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-technology-controls-monitoring-accelerator.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Technology Controls Monitoring Accelerator release notes

Version history for the GRC: Technology Controls Monitoring Accelerator on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACLs include the following enhancements:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
        -   Post-upgrade review for customized ACLs:
            -   If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 22.0.1 - March 2026**

    Changed: Prevent the use of working-draft control objectives in business logic.

-   **Version 21.1.0 - December 2025 \(Zurich\)**
    -   New: The GRC Technology Controls Monitoring Accelerator can now be activated or deactivated using the new 'Active' field on the GRC Choice record.
    -   Fixed: A read-only attribute has been added to fields designated as read-only, improving overall security.
-   **Version 21.0.1 - August 2025**

    Fixed: After installing GRC: Technology Controls Monitoring Accelerator, Indicator Templates show a banner message of "The plugin required for this indicator template is not installed" with no mention of what plugin can resolve it

-   **Version 18.1.0 - June 2024**

    Fixed: Updated CIS Version 8 indicator templates.

-   **Version 16.0.0 - February 2023**

    Fixed: Reduction in installation size of the application.

-   **Version 15.0.3 - August 2022**

    New: Move the sn\_irm\_shared\_cmn related files in GRC: Business user lite to if folder

-   **Version 12.0.2 - June 2021**

    New: Modules for Operational Status added to provide a list of all of your CIS Controls® and ISO 27002-based indicator templates mapped to specific CIS controls classified by domain, implementation group, and ISO controls.

-   **Version 12.0.1 - March 2021**

    Changed: Updated ability to monitor technology controls using pre-defined automated/scripted indicator templates


