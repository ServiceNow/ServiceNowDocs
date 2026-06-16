---
title: Security Incident Response integration with FireEye HX release notes
description: Version history for the Security Incident Response integration with FireEye HX on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-fireeye-hx.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response integration with FireEye HX release notes

Version history for the Security Incident Response integration with FireEye HX on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.1 - June 2026**

    New: Introduced Query range ACL's in FireEye HX.

-   **Version 1.1.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 1.0.14 - November 2024**

    New: Migration of Workflows to Flow Designer flows for Security Incident Response integration with FireEye Sighting Search, by enhancing the automation capabilities and process efficiency.

-   **Version 1.0.13 - March 2024**

    Fixed: Implemented parsing of fixed results from FireEye HX for "Get Network Statistics," "Get Running Services," "Get Running Processes," and "Get Logged On Users" capabilities. The data is now correctly associated with the Security Incident Response module.

-   **Version 1.0.11 - August 2023**

    Fixed: Access Token action parsing script in the Keep-Alive Header of the cloud instance.

-   **Version 1.0.10 - May 2023**

    New: Implement Table Cleaner rules for high impact/churn ServiceNow-owned tables from Security Incident Response for Security Incident Response integration with FireEye HX.

-   **Version 1.0.8 - February 2023**
    -   Fixed:
        -   Clean up of worknotes.
        -   FireEye business rule was deleting any other tiles available for running additional endpoints capability.
        -   Action Flatten Response giving null pointer exception.
        -   Support for Analyst workspace.
-   **Version 1.0.7 - November 2022**
    -   Changed: Utah Mandate: Update snc-app-parent version to 5.0.0.77
    -   Fixed:
        -   ServiceNow and FireEye Integration: When the Keep-Alive header is not present Get Token action fails for the FireEye cloud instance.
        -   Improve the logging for FireEye HX Integration.
-   **Version 1.0.6 - May 2022**

    Fixed: This release includes security fixes.

-   **Version 1.0.4 - December 2021**

    Fixed: This release includes security fixes.

-   **Version 1.0.3 - October 2021**

    Fixed: Added additional password-related policies

-   **Version 1.0.1 - August 2021**
    -   New:
        -   With FireEye Endpoint Security \(HX series\), organizations can proactively inspect, analyze, and contain known and unknown threats on any endpoint.
        -   The Gold Standard Security Incident Response integration with FireEye HX, makes it easier and efficient for Security Analysts to investigate and remediate security incidents in an instant without having to navigate between tools. You can use network containment to perform remediation actions on the endpoints, implement profiles to gather specific details about the host, and perform specific queries or actions on the endpoint.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

