---
title: Security Operations Metadefender Integration release notes
description: Version history for the Security Operations Metadefender Integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-metadefender-integration.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Operations Metadefender Integration release notes

Version history for the Security Operations Metadefender Integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.1 - June 2026**
    -   Fixed:
        -   Enhanced consistency and accuracy in HTTP status code handling within the file lookup workflow.
        -   Corrected reference field population in threat lookup result records for accurate source record linkage.
-   **Version 10.5.0 - August 2024**

    Changed: Migrated Threat Lookup workflows to flow designer.

-   **Version 10.4.0**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured duration/period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
-   **Version 2.0.3 - June 2021**

    Fixed: The hash lookup on observables is now working for the Metadefender integration.


