---
title: Vulnerability Response Integration Framework release notes
description: Version history for the Vulnerability Response Integration Framework application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-integration-framework.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration Framework release notes

Version history for the Vulnerability Response Integration Framework application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.0 - June 2026**

    Changed: Migrated query ACL definitions to the standard product codebase in Vulnerability Intelligence, improving maintainability and ensuring consistent access control enforcement.

-   **Version 1.4.1 - April 2026**

    Changed: Minor framework enhancements

-   **Version 1.3.0 - January 2026**

    Changed: Minor framework enhancements.

-   **Version 1.2.1 - December 2025**
    -   Fixed:
        -   PRB1925155:Enhanced role hierarchy for Integration Framework Administration.
            -   Added \`sn\_vul\_int\_fw.vif\_import\_admin\` role to \`sn\_vul.vulnerability\_admin\` role hierarchy, enabling vulnerability administrators to automatically inherit integration framework import administration capabilities.
-   **Version 1.1.2 - August 2025**
    -   Fixed:
        -   Added the following tabs to provide more details and performance metrics on Vulnerability Integration Run records:
            -   Detections
            -   Performance Statistics
            -   Performance Report
            -   Findings
-   **Version 1.0.5 - May 2025**

    This is a new framework built to support integrations with the Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.


