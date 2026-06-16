---
title: Security Incident Response integration with Zscaler release notes
description: Version history for the Security Incident Response integration with Zscaler on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-zscaler.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response integration with Zscaler release notes

Version history for the Security Incident Response integration with Zscaler on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.2.4 - June 2026**
    -   Fixed:
        -   Access issues for Security Analyst while querying tables.
        -   Flows reporting false failures when the Observable was already blocked or allowed.
-   **Version 11.2.3 - February 2026**

    Fixed: Populating observable category listing from Zscaler.

-   **Version 11.2.2 - December 2025**
    -   New:
        -   Upgraded dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.
        -   This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.
-   **Version 11.1.11 - August 2025**
    -   Fixed:
        -   Resolved an issue where the 'Zscaler Remove from URL Category' sub-flow was incorrectly left in draft state, preventing proper execution in production workflows. The sub-flow is now correctly published and active.
        -   Addressed a sandbox submission failure for Zscaler integrations where the system encountered error Cannot read property "Type" from undefined, errorCode:1. Root cause was due to missing data validation in sandbox processing. The fix ensures proper error handling and data validation to prevent runtime failures during submission.
-   **Version 11.1.3 - February 2025**
    -   Fixed:
        -   Resolved the issue where the 'Approval for Add to DenyList' flow was failing.
        -   Corrected the duplication of Approver records for the DenyList.
-   **Version 11.1.1 - November 2024**

    New: Migrated Workflows to Flow Designers flows. This update ensures a smoother transition and leverages the improved capabilities of Flow Designers.

-   **Version 11.1.0 - August 2024**

    New: The Zscaler integration is improved to provide configurable options for specifying different sets of approvers for both adding and removing observables.

-   **Version 11.0.17 - May 2024**

    New: Implemented the "Remove the observable from Denylist if present" checkbox when the same observable exists in the allow list and the analyst is trying to add the same observable to the Denylist again and vice versa.

-   **Version 11.0.14 - February 2024**
    -   Fixed:
        -   Added approval for Allowlist/Denylist in the activities section for the Security Incidents.
        -   The Findings field now displays all the observables.
-   **Version 11.0.13 - December 2023**

    Fixed: Addressed the security issues related to the misconfiguration of table/field ACLs within the com.snc.secops.zscaler plugin.

-   **Version 11.0.12 - November 2023**
    -   Fixed:
        -   The Zscaler URL validator regex had issues with some URLs.
        -   Threat lookup runs continuously even when there are no observables.
-   **Version 11.0.9 - August 2023**

    Fixed: Fixed an issue that prevented users from navigating to the flow designer when clicking from the security incident activity.

-   **Version 11.0.7 - May 2023**

    Fixed: Zscalar Integration creates an entry in the Zscaler URL Category List Entries table that immediately moves to the active state is ServiceNow, even if the record in the Zsclaer app is queued for activation.

-   **Version 11.0.6 - February 2023**

    Fixed: Zscaler integration is restricted from adding valid URL types.

-   **Version 11.0.3 - November 2022**
    -   Changed: Utah Mandate: changed app-sec-parent version to 5.0.0.77
    -   Fixed:
        -   Zscaler capability implementation records are not getting created in the Zscaler application scope.
        -   Localization issues.
        -   Filter Configurations for Zscaler capability are configured as capability-level filter conditions.
        -   Improve the logging for Zscaler integration.
-   **Version 11.0.2 - October 2021**
    -   Fixed:
        -   Fixed the issue with adding observables to a custom category
        -   Added additional password-related policies
-   **Version 11.0.0 - June 2021**
    -   Threat Look Up Analyst will be able to trigger reputation lookup’s on URL/IP/Domain
    -   Block/Allow URLs/IPs/Domain Analyst will be able to add URLs/Ips/Domain to tenant specific Block List/Allow List or other URL categories Support for periodic removal of entries from the list based on expiration value Support for Approval workflow Sandbox Report Look Up Analyst will be able to look up Sandbox report of MD5 hash and store it against the incident
    -   Create Security Incident out of Patient 0 alerts Support for ingestion of patient 0 alerts and create security incidents out of them

