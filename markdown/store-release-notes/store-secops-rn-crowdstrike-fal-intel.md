---
title: Security Operations CrowdStrike Falcon Intelligence integration release notes
description: Version history for the Security Operations CrowdStrike Falcon Intelligence integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-crowdstrike-fal-intel.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Operations CrowdStrike Falcon Intelligence integration release notes

Version history for the Security Operations CrowdStrike Falcon Intelligence integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.8.2 - June 2026**

    New: Added query range ACLS for CrowdStrike Intel.

-   **Version 10.8.1 - March 2026**

    Fixed: The CrowdStrike Indicators API now incorporates indicator types in threat lookup, resulting in improved malicious confidence.

-   **Version 10.8.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to improve security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 10.7.0 - August 2024**

    Changed: Migrated Threat lookup workflow to flow designer.

-   **Version 10.5.2 - March 2024**

    Fixed: Run threat lookup action for CrowdStrike Falcon Intelligence indicators now updates the results without the indicators.

-   **Version 10.5.1 - February 2023**

    New: Added type changes to support the Security Incident Response workspace.

-   **Version 10.5.0 - November 2022**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured duration/period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
-   **Version 10.4.1 - October 2021**
    -   New:
        -   Add Crowdstrike User string in outbound HTTP calls
        -   Added 'IOC Manager APIs' read and write permissions as required for the corresponding API key
    -   Fixed: Added additional password-related policies
-   **Version 10.3.3 - December 2020**

    Changed: With Key Management Framework plugin, developers will have an ability to manage keys used for Password2 fields through crypto module definition.

-   **Version 10.3.1 - October 2020**

    Changed: The integration now supports OAUTH2 authentication. This update requires the user to enter the API Client ID and the API Client Secret to authenticate and complete the configuration. If you are upgrading the integration from a previous version, then you must delete the existing configuration and set up a new configuration. The new integration supports OAUTH2 authentication. This update requires you to enter the API Client ID and the API Client Secret to authenticate and complete the configuration.

-   **Version 10.0.0 - September 2020**

    New: Implementation Flow to support the new capability framework \(v2.0\)

-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support the new capability framework \(v2.0\)


