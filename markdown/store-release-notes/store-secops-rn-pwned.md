---
title: Have I been pwned? integration release notes
description: Version history for the Security Operations Have I been pwned? integration on the ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-pwned.html
release: store
topic_type: reference
last_updated: "2025-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Have I been pwned? integration release notes

Version history for the Security Operations Have I been pwned? integration on the ServiceNow.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.1 - March 2025**

    Fixed: Version 10.5.1 of "Security Operations 'Have I been pwned?' Integration" includes a bug fix.

-   **Version 10.5.0 - August 2024**
    -   Changed: Migrated enrichment workflow to subflow.
    -   Fixed: Issue with sn\_ti\_lookup\_result.
-   **Version 10.4.1 - February 2023**

    New: Updated to support the Security Incident Response workspace.

-   **Version 10.4.0 - November 2022**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support Integration capability framework v2.0.

-   **Version 9.1.0**
    -   New: Upgraded the Have I been pwned? integration to use API v3
    -   Fixed:
        -   After a vendor updates the API contract, the integration works as expected
        -   Errors are logged correctly
-   **Version 8.0.8 - July 2019**
    -   New: Recertified for New York
    -   Fixed: Query performance fixes

