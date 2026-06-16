---
title: Secureworks Ticket Ingestion Integration for Security Operations release notes
description: Version history for the Secureworks Ticket Ingestion Integration for Security Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-secureworks-ticket-ingestion.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Secureworks Ticket Ingestion Integration for Security Operations release notes

Version history for the Secureworks Ticket Ingestion Integration for Security Operations.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.1.4 - June 2026**

    Fixed:Access issues for Security Analyst while querying tables.

-   **Version 11.1.3 - May 2026**

    Fixed: Access issues for Security Analyst while querying tables.

-   **Version 11.1.2 - February 2026**

    Fixed: Security Vulnerability via Client-Callable System-Run Subflow Code Execution.

-   **Version 11.1.1 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 11.0.18 - May 2024**

    The new UI dependency is removed.

-   **Version 11.0.16 - November 2023**

    Changed: Updated jQuery UI libraries to the latest versions.

-   **Version 11.0.13 - September 2022**
    -   Fixed:
        -   Improve the logging for Secureworks CTP ticket ingestion.
        -   Performance fix.
-   **Version 11.0.12 - June 2022**

    Fixed: Creating Blank SIR \(skipping SIR sequence\) when M2M mapping is done for Observable/CIs in Profile.

-   **Version 11.0.11 - March 2022**
    -   Fixed:
        -   Update AngularJS 1.4.8, platform mandate.
        -   Fixed the issue where the first ticket in Preview was not loading fine.
-   **Version 11.0.10 - December 2021**

    Fixed: UI changes

-   **Version 11.0.9 - November 2021**
    -   Fixed:
        -   Added additional password related policies.
        -   Fixed an error which occured when closing a SIR incident with the option 'Create knowledge article' enabled.
-   **Version 11.0.8 - August 2021**
    -   Fixed:
        -   Fixed an issue where the close ticket API call responds with a 400 error code when quotes were present.
        -   Fixed an issue where the error message "An error occurred while creating timeline entries." appeared when closing Security Incident created by SecureWorks when the option "Create knowledge article" was enabled.
-   **Version 11.0.5 - February 2021**

    Fixed: Fixed an issue where tickets were missing when the ISO format date was part of the Secureworks field that was mapped to ServiceNow field.

-   **Version 11.0.4 - December 2020**

    Changed: With Key Management Framework plugin, developers will have an ability to manage keys used for Password2 fields through crypto module definition.

-   **Version 11.0.2 - November 2020**

    Fixed: A fix has now been provided for the fetch sample events button for fetching the recent events, which was not working as expected.

-   **Version 11.0.1 - September 2020**

    New: The Secureworks CTP ticketing system is an application that supports the servicing needs of the Secureworks Managed Security Services \(MSS\) organizations. The Secureworks CTP ticket ingestion integration allows you to automatically fetch Secureworks CTP tickets and convert them into security incidents and enable automated response actions.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

