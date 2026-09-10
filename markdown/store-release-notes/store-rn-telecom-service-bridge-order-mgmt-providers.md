---
title: Service Exchange Order Management for Providers release notes
description: Version history for the Service Exchange Order Management for Providers application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-service-bridge-order-mgmt-providers.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Technology Provider Service Management version history release notes, ServiceNow Store version history release notes]
---

# Service Exchange Order Management for Providers release notes

Version history for the Service Exchange Order Management for Providers application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.4.10 - September 2026**
    -   Service Exchange Order Management for Providers — v2.4.10
        -   Fixed: Addressed release-verification issues with config-failure errors and stale inactive offerings on the request page. \(PRB2076821\)
    -   Service Exchange for Providers — v2.4.10
        -   Fixed
            -   Remote Choice Definitions with Account Secure could fail lookups for external integration users. \(PRB2054434\)
            -   An emoji in the off-boarding message blocked translation when switching languages. \(PRB2032117\)
        -   Changed: Provider Task activity stream now defaults to Additional Comments instead of Work Notes.
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
        -   New:
            -   Added a clearer down-connection warning about data loss after 7+ days.
            -   Added a notification to admins when the Admin group has no users.
            -   Added warning messages for missing roles \(itil, cmdb\_read, personalize, import\_admin\).
-   **Version 2.2.25 - August 2026 \(Australia\)**

    Security enhancements applied.

-   **Version 2.1.46 - August 2026 \(Zurich\)**

    Security enhancements applied.

-   **Version 2.3.29 - August 2026**
    -   Fixed a security issue where a Foundation Data Sync manager could delete, archive, or modify another company's offering, subscription, or CMDB records. \(PRB2028446\)
    -   Fixed a security issue where a specially crafted company name or field label could execute a malicious script when displayed in a Foundation Data Sync error message. \(PRB2028450\)
-   **Version 2.3.18 - June 2026**
    -   Connections tab in the Service Exchange Center: Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.
    -   Improved consumer registration and onboarding: Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.
    -   Improved FDS capabilities:
        -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
        -   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
        -   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
        -   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.
    -   Journal Field Framework enhancements:
        -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
        -   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting
    -   Group-based persona assignments for Remote Catalog: Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.
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
-   **Version 2.1.36 - April 2026 \(Zurich\)**
    -   New:
        -   Added translations
        -   Change name from Service Bridge to Service Exchange
-   **Version 2.0.75 - April 2026 \(Yokohama\)**
    -   New:
        -   Added translations
        -   Change name from Service Bridge to Service Exchange
-   **Version 2.3.9 - March 2026**
    -   New:
        -   Service Exchange Center
            -   Introduced the unified Health Dashboard for improved visibility into connections through a new Heartbeat capability, more accurate connection status, enhanced search and filtering, and centralized issue tracking with validation and resolution.
        -   Automated Onboarding
            -   Delivered automated Consumer–Provider onboarding with secure registration, automated pre‑ and post‑onboarding suite validations, improved retry and timeout handling including one‑sided consumer offboarding, and clearer onboarding states with actionable error messaging and recovery.
        -   Service Exchange Core
            -   Improved transport reliability, strengthened Remote Task error handling, enabled provider‑to‑consumer task variable updates, and ensured Remote Choice values remain accurate.
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
-   **Version 2.1.33 - March 2026 \(Zurich\)**

    Service Bridge renamed to Service Exchange

-   **Version 2.0.70 - March 2026 \(Yokohama\)**

    Service Bridge renamed to Service Exchange

-   **Version 2.2.5 - September 2025**

    No updates.

-   **Version 2.2.2 - August 2025**
    -   New:
        -   Journal Field Framework \(JFF\) - Remote Task
            -   Support all journal field types
            -   Support for historical journal sync
            -   Write journals as the real user
        -   Foundation Data Sync \(FDS\) \(Provider to Consumer Only\)
            -   Non-CMDB tables /w Transform Maps
            -   CMDB /w IH ETL and IRE
            -   Supported tables: CMDB, Asset, User, Group, Location, Company, Department
        -   Health Dashboard
            -   Proactive Issue Detection: Instance scan checks identify inconsistencies early, maintaining health via the Health Dashboard for findings and errors.
            -   Key Benefits: Enhances integration stability, reduces troubleshooting, offers error solutions, boosts productivity.
            -   Scan Suites: Provide on-demand/scheduled scans
        -   Magic Links: SSO login for consumers directly to resources in the provider instance
    -   Changed: Remote Task uses the new journal field framework.
    -   Fixed:
        -   Proper handling of HTML tags in journal fields
        -   Identity is missing in clone.
        -   \(Clone\) Remove Excludes on OOB table sys\_alias and replace with a post clone cleanup script
        -   Flow "Update Error Message on Remote Task" called but errors out after work note added
        -   \(RPS\) Ensure the OAuth tokens do not expire due to no transactions within 24 hours of expiration
        -   Service Bridge needs logging to inform customers when attachments are dropped, for example, per the Restrict File Extensions system property
        -   Related lists disappearing after adding or removing the related list on the table, Remote record producer
        -   RTD getting deleted with Refresh entitlements, Scheduled job
        -   "Create Remote Task for Provider" and "Create Remote Task for Consumer" buttons are visible for users without the role "sn\_sb.remote\_task\_creator"
        -   Clone - After clone, in target instances, existing/old Provider tasks data\(Variable, Comments, and attachments\) are missing.
        -   Reference variables do not list any values when certain variable attributes are set
        -   RRP Catalog Item Categories clone cleanup script errors and stops all clone cleanup scripts from completing
        -   RRP Catalog Item Categories cleanup script fails, causing all the subsequent cleanup scripts to not run post-clone
        -   The Change Request state \(close\) is not transferring to the Service Bridge Provider when the request is closed
-   **Version 2.1.30 - June 2025**

    No updates this release.

-   **Version 1.0.5 - February 2025**

    No updates this release.

-   **Version 1.0.0 - August 2024**

    Providers often struggle with inefficiencies in their ordering processes when working with customers who have their own ServiceNow instances. This lack of integration results in poor communication, manual order handling, and delays in fulfilling orders, negatively impacting service delivery and customer satisfaction. Order Management for Providers with Service Bridge offers seamless integration and automation to transform the ordering experience, making it faster, more accurate, and more satisfying for both providers and customers.


