---
title: Service Exchange Order Management for Providers release notes
description: Version history for the Service Exchange Order Management for Providers application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-service-bridge-order-mgmt-providers.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Service Exchange Order Management for Providers release notes

Version history for the Service Exchange Order Management for Providers application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

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


