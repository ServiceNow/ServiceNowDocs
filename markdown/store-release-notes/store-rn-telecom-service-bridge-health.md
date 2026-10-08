---
title: Service Bridge Health release notes
description: Version history for the Service Bridge Health on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-service-bridge-health.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Technology Provider Service Management version history release notes, ServiceNow Store version history release notes]
---

# Service Bridge Health release notes

Version history for the Service Bridge Health on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.4.17 - October 2026**

    Foundation Data Sync v2.4.15

    Changed: Improved the attachment sync strategy between provider and consumer.

    Service Exchange Remote Process Sync Transport v2.4.15

    Fixed

    -   Tightened OAuth client-credential token scope, limiting what a token can access. \(PRB2067950\)
    -   Removed the snc\_internal role requirement from the REST API that failed if the role was missing \(PRB2076065\)
    Service Exchange Health v2.4.15

    -   New
        -   When a connection goes down, some known issues are now auto-diagnosed and fixed, with the outcome logged on the resulting health issue.
        -   Connection health now tracks slow/down occurrences, resetting monthly.
        -   Overridden consumer updates now generate a visible error record instead of failing silently.
        -   Existing error code 999 unknown health issues converted to known issue types
    -   Changed: Stale slow/down status indicators now clear automatically once a connection recovers.
    -   Fixed: Fixed translation issues in scan-suite filtering, offboarding, and a connection status label. \(PRB2038126\)
    Service Exchange for Consumers v2.4.15

    -   New: Error code 999 health issues now include more context on what's affected.
    -   Fixed
        -   Fixed a localization issue found during a routine scan. \(PRB2083235\)
        -   Fixed embedded images appearing broken, or as raw HTML, when synced to the provider. \(PRB2076772\)
    Service Exchange for Providers v2.4.15

    -   New: Existing error code 999 unknown health issues converted to known issue types
    -   Fixed: Fixed catalog item variable-set order not carrying over when published as a Remote Record Producer. \(PRB2074741\)
    Service Exchange Base v2.4.15

    -   New
        -   Admins can upgrade a connection from legacy OAuth to Client Credentials directly from the connection record.
        -   Sync job frequency is now configurable via a system property instead of fixed.
    -   Fixed
        -   Tightened OAuth client-credential token scope, limiting what a token can access. \(PRB2067950\)
        -   Fixed an issue blocking simultaneous inbound and outbound transforms on the same field. \(PRB2075724\)
        -   Fixed a Remote Record Producer publish issue where a dependent variable kept pointing to the prior version. \(PRB2074843\)
        -   Fixed a missing translation label on the Case table. \(PRB2083234\)
        -   The Service Exchange Admins group is no longer selectable as a task/problem assignment group. \(PRB2079342\)
    v2.4.15 Foundation Data Sync for Consumers Foundation Data Sync for Providers, Service Exchange Order Management for Providers Transporter: These releases update the application to version 2.4.15 with no functional changes outside of the mentions above.

-   **Version 2.4.10 - September 2026**
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
    -   Service Exchange for Consumers — v2.4.10
        -   Fixed
            -   Attachments could queue unnecessary background jobs regardless of connection state. \(PRB2070888\)
            -   A remote task wasn't created when its trigger condition referenced a child-table-only field. \(PRB2070471\)
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
-   **Version 1.0.17 - August 2026 \(Australia\)**

    Security enhancements applied.

-   **Version 2.3.18 - June 2026**
    -   Connections tab in the Service Exchange Center: Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.
    -   Improved consumer registration and onboarding: Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.
    -   Improved FDS capabilities:
        -   Improve your connection experience by syncing Knowledge Base articles between provider and consumer instances.
        -   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
        -   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
        -   Improved compliance through restricted data sync from non-production instances to production instances for CMDB tables.
    -   Journal Field Framework enhancements:
        -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
        -   Configure journal fields, such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting.
    -   Group-based persona assignments for Remote Catalog: Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.
-   **Version 2.3.15 - May 2026**
    -   Fixed:
        -   Inbound Transform Execution
            -   Resolved an issue where inbound transforms could fail to execute due to permission-related constraints, ensuring reliable data ingestion and processing.
        -   Connection Entitlements Retention
            -   Fixed a condition where entitlements could be lost after a connection was interrupted and later re-established. Entitlements are now consistently preserved across reconnections.
        -   Improved Onboarding Error Handling
            -   Enhanced onboarding behavior so that, if an error occurs in an onboarding flow, a clear error message is presented instead of the process remaining in a “Work in Progress” state.
-   **Version 1.0.7 - April 2026**
    -   New:
        -   Added translations
        -   Change name from Service Bridge to Service Exchange
-   **Version 2.3.9 - March 2026**
    -   New:
        -   Service Exchange Center
            -   Introduced the unified Health Dashboard for improved visibility into connections through a new Heartbeat capability, more accurate connection status, enhanced search and filtering, and centralized issue tracking with validation and resolution.
        -   Documentation
            -   Restructured Service Exchange documentation.
-   **Version 1.0.4 - November 2025**

    Fixes: Scan tasks are automatically closed when subsequent executions produce no new findings.

-   **Version 1.0.3 - September 2025**
    -   Fixed:
        -   Updated scan check to handle "User Not Authenticated" intermittent issue with RPS \(PRB1924176\)
        -   Improved pre-onboarding scan check suite \(PRB1917753\)
-   **Version 1.0.1 - August 2025**

    This application contains the Instance scan audit checks for Service Bridge.


**Parent Topic:**[ServiceNow Store - Technology Provider Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

