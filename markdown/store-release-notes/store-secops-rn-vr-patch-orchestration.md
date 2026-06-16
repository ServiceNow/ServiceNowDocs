---
title: Vulnerability Response Patch Orchestration release notes
description: Version history for the Vulnerability Response Patch Orchestration application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-patch-orchestration.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Patch Orchestration release notes

Version history for the Vulnerability Response Patch Orchestration application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

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


