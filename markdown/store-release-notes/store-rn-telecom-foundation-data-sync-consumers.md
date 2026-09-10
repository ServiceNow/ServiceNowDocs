---
title: Foundation Data Sync for Consumers release notes
description: Version history for the Foundation Data Sync for Consumers application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-foundation-data-sync-consumers.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Technology Provider Service Management version history release notes, ServiceNow Store version history release notes]
---

# Foundation Data Sync for Consumers release notes

Version history for the Foundation Data Sync for Consumers application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.4.10 - September 2026**
    -   Foundation Data Sync for Consumers — v2.4.10: No functional changes.
    -   Service Exchange for Consumers — v2.4.10
        -   Fixed
            -   Attachments could queue unnecessary background jobs regardless of connection state. \(PRB2070888\)
            -   A remote task wasn't created when its trigger condition referenced a child-table-only field. \(PRB2070471\)
    -   Foundation Data Sync — v2.4.10
        -   Fixed
            -   Multi-value list fields could truncate when a later batch sent more data than the first. \(PRB2068326\)
            -   Requesting an offering referencing a table missing on the requester blocked further requests. \(PRB2063217\)
            -   Initial payload sync could duplicate or skip records if source data changed mid-sync. \(PRB2061531\)
            -   Batches after the first could stop processing during bulk sync. \(PRB2068330\)
            -   Knowledge article attachment sync now correctly handles tables that extend a base table.
        -   Changed: Synced KB articles now default to including the provider name in the target KB name.
    -   Service Exchange Base — v2.4.10
        -   Fixed
            -   Near-simultaneous updates on provider and consumer could drop one side's change. \(PRB2029744\)
            -   output.ignore=true on a transform didn't actually exclude the field from the sync payload. \(PRB2066768\)
            -   The Case table lacked a proper label/plural, showing an auto-generated name to some users. \(PRB1923483\)
            -   A multi-row variable set on a record producer overwrote all rows with the last row's value. \(PRB2061638\)
        -   Changed: Restart Connection after a clone/upgrade now also reactivates capture definitions automatically.
        -   New: Added a scheduled sweep to reactivate capture definitions left inactive after a clone/upgrade.
    -   Service Exchange Remote Process Sync Transport — v2.4.10
        -   Fixed
            -   Onboarding could time out on slow connections, leaving OAuth credentials empty. \(PRB2064896\)
            -   OAuth credentials during onboarding were sent via URL query params instead of the request body. \(PRB2060125\)
    -   Transporter — v2.4.10: No functional changes.
    -   Service Exchange Health — v2.4.10
        -   Fixed
            -   Integration-user-naming scan check didn't validate the required prefix. \(PRB2023585\)
            -   Some pre-onboarding scan failures didn't generate an Issue record, hiding the block reason. \(PRB2025384\)
            -   Tightened ACLs on Health records; removed a console log exposing connection data. \(PRB2071380\)
            -   Fixed message alignment and a duplicate message on the admin-group scan check. \(PRB2067053\)
            -   Connection Dashboard now shows accurate inbound/outbound transport queue backlog counts.
        -   Changed: Consolidated two magic-link scan checks into one, gated on whether magic links are enabled.
        -   New
            -   Added a clearer down-connection warning about data loss after 7+ days.
            -   Added a notification to admins when the Admin group has no users.
            -   Added warning messages for missing roles \(itil, cmdb\_read, personalize, import\_admin\).
-   **Version 2.2.25 - August 2026 \(Australia\)**

    Security enhancements applied.

-   **Version 2.3.29 - August 2026**

    This release updates the application to version 2.3.29 with no functional changes.

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
            -   Delivered automated Consumer–Provider onboarding with secure registration, automated pre‑ and post‑onboarding suite validations, improved retry and timeout handling including one‑sided consumer offboarding, and clearer onboarding states with actionable error messaging and recovery.
        -   Service Exchange Core
            -   Improved transport reliability, strengthened Remote Task error handling, enabled provider‑to‑consumer task variable updates, and ensured Remote Choice values remain accurate.
        -   Foundation Data Sync
            -   Added bi‑directional data sync from Consumer to Provider, improved attachment handling, introduced automated field mapping, and enhanced visibility into offerings, subscriptions, and revisions.
        -   Documentation
            -   Restructured Service Exchange documentation.
    -   Fixed:
        -   Improved resilience of RPS outbound \(PRB1918189\)
        -   RPS connection failures caused by malformed attachments \(PRB1969541\)
        -   Additional comments are not updated as expected \(PRB1984220\)
        -   Improved retry behavior during onboarding and Offboarding \(PRB1925551\)
        -   Corrected CI sync behavior after initial payload \(PRB1961406\)
        -   Improved handling of inbound email attachments \(PRB1920319\)
        -   Resolved Clone script conflicts \(PRB1966599\)
-   **Version 2.2.6 - November 2025**
    -   Fixed:
        -   Offerings now populate the company field correctly
        -   The Consumer active revision field on the entitlements table now shows the correct number
-   **Version 2.2.5 - September 2025**

    Foundation Data Sync for Consumers enables customers to request and receive foundational data from their providers without the need for a costly third-party integration.


**Parent Topic:**[ServiceNow Store - Technology Provider Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

