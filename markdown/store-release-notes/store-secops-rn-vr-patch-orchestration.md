---
title: Vulnerability Response Patch Orchestration release notes
description: Version history for the Vulnerability Response Patch Orchestration application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-patch-orchestration.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Vulnerability Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# Vulnerability Response Patch Orchestration release notes

Version history for the Vulnerability Response Patch Orchestration application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.3.6 - September 2026**
    -   New: Framework enhancements to support multiple patch to multi asset/asset group deployments.
    -   New:
        -   Enhanced Patch Orchestration with advanced scheduling and deployment options. Customers can now schedule and orchestrate patch deployments directly within the Patch Orchestration module, including support for deployment rings and integration of additional patch and endpoint metadata from Tanium.
        -   Improved patch-to-vulnerability mapping and rollup logic. The system now supports enhanced matching criteria between patches and vulnerabilities, with new fields for knowledge base URLs, patch size, and confidence score, increasing mapping accuracy and visibility.
        -   SCCM integration now supports JDBC queries. Customers can leverage JDBC-based integration for SCCM, replacing previous WMI-based methods for improved reliability and compatibility.
    -   Changed:
        -   Schedule Patch UI migrated to app-vul-patch-orch. The Patch Deployment section is now visible in the Change Request creation modal when both app-vul-resp and app-vul-patch-orch are installed. When only app-vul-resp is installed, the Patch Deployment section is hidden, ensuring a streamlined user experience.
        -   Fluent Migration completed for app-vul-patch-orch. The package.json has been added and validated, aligning with Fluent Migration Milestone 1 requirements.
-   **Version 30.2.1 - April 2026 \(USEM\)**

    Fixed: A security vulnerability in the Patch Orchestration scheduling component where a client-callable interface lacked proper input validation, which permitted unauthorized deletion of arbitrary records. The fix enforces strict access controls to ensure delete operations are only permitted for authorized users on permitted records.

-   **Version 2.2.6 - April 2026**

    Fixed: Resolved a security vulnerability in the Patch Orchestration scheduling component where a client-callable interface lacked proper input validation, allowing unauthorized deletion of arbitrary records. The fix enforces strict access controls to ensure delete operations are only permitted for authorized users on permitted records.

-   **Version 30.2.0 - January 2026 \(USEM\)**

    Changed: The approval rules for patch orchestration are unified and similar to the unified approval rules for the Exception Management for Unified Security Exposure Management plugin \(sn\_sec\_exception\) and can apply to multiple tables.

-   **Version 2.2.5 - May 2025**

    New: The patch orchestration data model is extended to integrate with ITSM systems seamlessly.

-   **Version 2.1.1 - November 2024**

    Fixed: Performance improvements for the patch rollup scheduled job that rolls up the patches to vulnerability and vulnerable item \(VIT\) records. You might see that the scheduled job runs more quickly.

-   **Version 2.0.6 - February 2024**

    New: Localization support changes done as part of this release.

-   **Version 2.0.5 - December 2023**

    Fixed: Removed unnecessary ACLs in the 'com.snc.vulnerability.patch\_orch' plugin.

-   **Version 2.0.3 -August 2022**
    -   New: Remediation owners can navigate to the scorecards and view the preferred patch associated with the configuration items. They can use this information to remediate the critical vulnerabilities in the assets that they own.
    -   Fixed: Remediation Owners were not able to view the list "Patches -&gt; All". This issue has now been fixed.
-   **Version 2.0.1 - March 2022**

    The Vulnerability Response Patch Orchestration application correlates patches with vulnerable items and provides visibility into the missing patches for your critical vulnerable items and assets.


