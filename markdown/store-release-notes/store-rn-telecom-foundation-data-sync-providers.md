---
title: Foundation Data Sync for Providers release notes
description: Version history for the Foundation Data Sync for Providers application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-foundation-data-sync-providers.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Foundation Data Sync for Providers release notes

Version history for the Foundation Data Sync for Providers application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.18 - June 2026**
    -   Improved capabilities:
        -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
        -   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
        -   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
        -   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.
-   **Version 2.3.15 - May 2026**
    -   Fixed:
        -   Inbound Transform Execution
            -   Resolved an issue where inbound transforms could fail to execute due to permission-related constraints, ensuring reliable data ingestion and processing.
        -   Connection Entitlements Retention
            -   Fixed a condition where entitlements could be lost after a connection was interrupted and later re-established. Entitlements are now consistently preserved across reconnections.
        -   Improved Onboarding Error Handling
            -   Enhanced onboarding behavior so that, if an error occurs in an onboarding flow, a clear error message is presented instead of the process remaining in a “Work in Progress” state.
-   **Version 2.2.13 - April 2026 \(Australia\)**
    -   New:
        -   Added translations
        -   Change name from Service Bridge to Service Exchange
-   **Version 2.3.12 - March 2026**
    -   New:
        -   Service Exchange Center
            -   Introduced the unified Health Dashboard for improved visibility into connections through a new Heartbeat capability, more accurate connection status, enhanced search and filtering, and centralized issue tracking with validation and resolution.
        -   Automated Onboarding
            -   Delivered automated Consumer&amp;ndash;Provider onboarding with secure registration, automated pre‑ and post‑onboarding suite validations, improved retry and timeout handling including one‑sided consumer offboarding, and clearer onboarding states with actionable error messaging and recovery.
        -   Service Exchange Core
            -   Improved transport reliability, strengthened Remote Task error handling, enabled provider‑to‑consumer task variable updates, and ensured Remote Choice values remain accurate.
        -   Foundation Data Sync
            -   Added bi‑directional data sync from Consumer to Provider, improved attachment handling, introduced automated field mapping, and enhanced visibility into offerings, subscriptions, and revisions.
        -   Documentation
            -   Restructured Service Exchange documentation.
    -   Fixed:
        -   Improved resilience of RPS outbound \(PRB1918189\)
        -   RPS connection failures caused by malformed attachments \(PRB1969541\)
        -   Additional comments are not updated as expected \(PRB1984220\)
        -   Improved retry behavior during onboarding and Offboarding \(PRB1925551\)
        -   Corrected CI sync behavior after initial payload \(PRB1961406\)
        -   Improved handling of inbound email attachments \(PRB1920319\)
        -   Resolved Clone script conflicts \(PRB1966599\)
-   **Version 2.2.5 - September 2025**
    -   Foundation Data Sync \(FDS\) enables the structured, periodic sharing of data from provider to consumer instances. It ensures that consumers have access to accurate, up-to-date foundational data from providers, supporting better service delivery and operational alignment.
    -   FDS is a data synchronization mechanism that enables a provider instance to share foundational data with consumer instances on a scheduled basis, such as daily, weekly, or monthly.
    -   FDS supports all CMDB tables and the following non-CMDB tables: Asset, User, Group, Location, Company, and Department.

**Parent Topic:**[ServiceNow Store - Technology Provider Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

