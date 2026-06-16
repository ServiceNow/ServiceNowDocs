---
title: Microsoft Graph Security API Alert Ingestion integration for Security Operations release notes
description: Version history for the Microsoft Graph Security API Alert Ingestion integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-microsoft-graph-security-api-alert.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Microsoft Graph Security API Alert Ingestion integration for Security Operations release notes

Version history for the Microsoft Graph Security API Alert Ingestion integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.3 - June 2026**

    Changed: Replaced hardcoded endpoint path to system properties.

-   **Version 10.5.2 - March 2026**

    Fixed: Reintroduced a new column to filter alerts.

-   **Version 10.5.1 - February 2026**

    Fixed: Successful validation message getting displayed during configuration tile validation despite invalid credentials.

-   **Version 10.5.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 10.4.13 - August 2025**

    Fixed: Improved Handling of Next Poll Date for Microsoft Graph Security Alert Integration on HTTP Failures.

-   **Version 10.4.8 - May 2024**

    The dependency on the new UI is removed.

-   **Version 10.4.7 - November 2023**

    Fixed: Updated the dependent application's \(Common Plugin for SecOps SIEM Integration\) version to the latest version.

-   **Version 10.4.6 - May 2023**
    -   New:
        -   The Microsoft Graph Security API - ServiceNow Security Incident Response integration has been upgraded to V2.0 API.
        -   Provides you with the ability to map MITRE ATT&amp;CK data in the Graph Security alert to the MITRE ATT&amp;CK field in the security incident.
    -   Fixed:
        -   One-Time Retrieval is not working on the scheduling page of the profile when we change the date format to dd-MM-YYYY for the Graph Security API.
        -   Microsoft Graph Security API Alert Ingestion Integration: Dark theme is not applied to all fields.
-   **Version 10.4.5 - September 2022**

    Changed: Performance fix.

-   **Version 10.4.4 - June 2022**

    Fixed: When there is a Business Rule on Observable/CI and task M2M records, which updates the SIR fields automatically. This occurs since SIR was not persisted at the creation time using SIEM, and the SIR fields are not getting updated. This issue has been resolved, and now SIR would persist first in DB, and then the M2M records are created.

-   **Version 10.4.2 - December 2021**

    Fixed: UI fixes.

-   **Version 10.4.1 - October 2021**

    Fixed: Added additional password-related policies.

-   **Version 10.4.0 - May 2021**
    -   Changed: When multiple alert fields are mapped to a SIR field and if one of the alert field value is NULL or blank, that doesnt empty the SIR field instead will map the values available.
    -   New: Alerts ingestion mechanism is improved to avoid missing alerts injestion during polling intervals
-   **Version 10.3.3 - December 2020**

    Changed: With Key Management Framework plugin, developers will have an ability to manage keys used for Password2 fields through crypto module definition.

-   **Version 10.0.6 - May 2020**
    -   The Microsoft Graph Security API is an intermediary service \(or broker\) that provides a single programmatic interface to connect multiple security providers \(Native to Microsoft as well as ServiceNow Partners\).
    -   The Microsoft Graph Security Alert Ingestion integration allows you to automatically fetch alerts from multiple security providers and convert them into security incidents and enable automated response actions.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

