---
title: Vulnerability Response Integration Framework release notes
description: Version history for the Vulnerability Response Integration Framework application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-integration-framework.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# Vulnerability Response Integration Framework release notes

Version history for the Vulnerability Response Integration Framework application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.6.4 - September 2026**
    -   Fixed: Resolved an issue where certain access control configurations in the Vulnerability Response Integration Framework referenced invalid user roles.
    -   New: Fix information is now imported for vulnerable items from Armis. The VR Integration Framework supports importing and displaying fix details for vulnerable items \(VITs\) sourced from Armis, enabling users to view remediation options directly within the platform.
-   **Version 1.6.2 - August 2026**

    Enhancements to the VR Integration Framework to support fix information on vulnerable items \(VITs\) imported from Armis.

-   **Version 1.6.0 - July 2026**
    -   New: Added \_determineStartTime\(\)toVRIntegrationFrameworkBase, giving integration implementations a standardized hook to compute the delta start time for incremental imports.
    -   Fixed:
        -   Resolved an issue where the integration import queue would get stuck when a job was in an Error state with a non-empty "Processed by \(Trigger\)" value, blocking all subsequent queued entries from processing.
        -   Applied a security fix to enforce read-only field restrictions, addressing the Australia Security Directive for field-level access control.
    -   Changed: Added the integration run number to the integration run list view for easier identification.
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


