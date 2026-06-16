---
title: Virus Total integration release notes
description: Version history for the Security Operations VirusTotal integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-virustotal.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Virus Total integration release notes

Version history for the Security Operations VirusTotal integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.4.1 - December 2025**

    New: Upgraded dictionary-level read-only fields to Strict Read-Only to improve security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 10.4.0 - August 2024**
    -   Changed: Migrated Threat lookup workflows to flow designer.
    -   Fixed: Threat lookup of URL fails if it is not present in the existing VT reports.
-   **Version 10.3.6 - January 2024**

    Fixed: Added a new option on the configuration to send URLs as hashes for threat lookup, to protect the users' privacy on the integration.

-   **Version 10.3.4 - May 2023**
    -   New:
        -   Added private file scan endpoints/rest calls.
        -   If checkbox VT private scanning is selected on the configuration tile, then the private endpoints are getting hit for the observable threat look-up of file type.
        -   The older v2 rest calls are removed.
    -   Fixed:
        -   For file analysis the wrong endpoint was hitting in the current implementation, this is now fixed.
-   **Version 10.3.2 - February 2023**

    New: Added changes to support the Security Incident Response workspace.

-   **Version 10.3.1 - November 2022**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
-   **Version 10.2.0 - May 2022**

    Changed: Upgraded from Version 2 APIs to Version 3 APIs.

-   **Version 10.1.0 - September 2020**

    New: Updated VirusTotal integration to support file type observable security change.

-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support the new capability framework \(v2.0\)

-   **Version 8.0.8 - July 2019**
    -   New: Recertified for New York
    -   Fixed: Query performance fixes

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

