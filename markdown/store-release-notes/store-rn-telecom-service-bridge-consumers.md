---
title: Service Exchange for Consumers release notes
description: Version history for the Service Exchange for Consumers application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-service-bridge-consumers.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Service Exchange for Consumers release notes

Version history for the Service Exchange for Consumers application on the ServiceNow Store.

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

    Do not upgrade your ServiceNow instance to the Australia release if you rely on Service Exchange. A known RPS issue prevents Service Exchange from functioning correctly. Proceed with the upgrade only after Australia Patch 1 becomes available.New

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

-   **Version 2.2.6 - November 2025**
    -   Fixed:
        -   Custom URL support improved
        -   Added a pre-insert warning on Provider Connection to run the pre-onboarding suite and check the Health Dashboard before proceeding.
        -   Fixed an issue where Variable Sets on the target instance could be deleted after cloning from the source.
-   **Version 2.2.5 - September 2025**
    -   Fixed:
        -   Provider tasks are showing internal values for remote choice variables in variable sets instead of their display values \(PRB1925091\)
        -   Glide Sandbox Bypass in Service Bridge for Consumers \(PRB1923983\)
-   **Version 2.2.2 - August 2025**
    -   New:
        -   Journal Field Framework - Remote Task
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
        -   Magic Links: SSO login for consumers allowing direct access to resources in the provider instance.
    -   Changed: Remote Task uses the new journal field framework.
    -   Fixed:
        -   Service Bridge - Proper handling of HTML tags in journal fields
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
    -   Fixed:
        -   Strict Mode Related Error On Parent Record Insert \(PRB1861010\)
        -   Journal sync key improvements \(PRB1866365\)
        -   Mapping assist not visible despite enabled skill \(PRB1857473\)
-   **Version 2.0.65 - June 2025**

    Fixed: Improved journal field sync for edge cases \(PRB1886817\).

-   **Version 2.1.20 - February 2025**
    -   New:
        -   Remote Catalog
            -   Script support - Catalog client scripts, and UI Policy scripts
            -   Publish to Service Bridge from local catalog items
            -   Consumer Variable sets - Consumers can add variables to provider catalogs for use in Consumer Pre-Flows
        -   Now Assist for TMT
            -   Transform Mapping Assist - Use GenAI to automatically generate transform lines for choice fields.
    -   Fixed:
        -   PRB1823044 - Company mismatch preventing some transforms from being executed
        -   PRB1787085 - Not able to sync attachments from provider to consumer using RPS inbound subflow
        -   PRB1782692 - Unable to set new field value when returning null or empty.
-   **Version 2.0.30 - October 2024**
    -   Fixed:
        -   PRB1796288 - \[Consumer\] Duplicate Remote Tasks getting created for the same remote task definition with different revisions
        -   PRB1803440 - \[Consumer\] Remote Task Creation on Consumer is Getting Blocked for Revision 1 while Revision 2 is Pending on the Consumer instance
        -   PRB1797924 - \[Consumer\] Updates to parent tasks do not sync data to remote tasks if user is in different domain
        -   PRB1800310 - Deletions and status changes of existing configurations need to be sent to consumers on 1.x.x when provider is on 2.x.x
        -   PRB1799772 - Can't Edit Remote Catalog Items after Service Bridge Upgrade
        -   PRB1795471 - Off-board button of Service Brige 2.0.2 is deleting all variable set
        -   PRB1787307 - Service Bridge Connection breaks after cloning over the instance
-   **Version 2.0.20 - August 2024**
    -   New:
        -   Mismatched version support
            -   Enables providers and consumers to be on different versions of Service Bridge
        -   Configuration Revisions
            -   Adds the ability to upgrade and publish new Remote Record Producers, and Remote Task Definitions without breaking customers that have not upgraded yet.
        -   Consumer Pre-Flows
            -   Adds a Flow field to Remote Record Producers for consumers allowing them to run processes, like approvals, before syncing a provider task
        -   Maintain RRP GUID between instances
            -   Remote Record Producers are now created with the same sys\_ids on the consumer as on the provider enabling consumers to reliably create processes that reference them.
    -   Changed: Configuration Revisionsis a change to how configurations like RRPs, and RTDs are published and edited. New records are created for each publish to retain existing functionality for consumers that have not yet updated.
    -   Fixed:
        -   PRB1759812 Service Bridge Consumer: The Catalog Ui Policy actions are getting sys\_id in the consumer instance
        -   PRB1744459 RRP: Sync RRP variable auto-populate fields to consumer
        -   PRB1755334 Error setting up new Service Bridge Consumer, "Failed retrieving OAuth Profile"- when 2 consumers register at same time
-   **Version 1.1.2 - March 2024**
    -   Fixed:
        -   In some instances, the OAuth Cryptographic Module has its access policy set toReject,which will block Service Bridge's ability to complete registration for a consumer.
            -   We added an error message in the Consumer instance on the Provider Connection record with instructions to resolve this issue if it exists.
-   **Version 1.1.0 - February 2024**
    -   New:
        -   Added an error table and known error codes to support troubleshooting
        -   Localization Support
        -   Added AES 256 encryption to support registration between all instance types including on-prem
        -   Doc updates to improve enablement
        -   Added variable set and multi-row variable set support to Remote Catalog items
    -   Changed: Consumer Registration now defaults to Service Bridge encryption instead of Key Management Framework
    -   Fixed:
        -   Various cosmetic issues resolved
        -   If contact changes on the consumer registration task after inert the new contact will receive the required consumer role.
        -   Duplicate attachment issue on Remote Record producers
        -   RPS outbound state going into error on Utah and earlier instances
-   **Version 1.0.5 - January 2024**
    -   Fixed:
        -   ACL cleanup
        -   Security fixes
-   **Version 1.0.4 - December 2023**
    -   New:
        -   Added a consumer Instance ID field to the consumer registration task
        -   Added OauthKMF Key Exchange to support updated security controls. This update includes a Retry key exchange request UI Action that appears on the Provider connection record if there is any issue with the key exchange.
    -   Fixed:
        -   PRB1712507/PRB1677764 - duplicate attachments
        -   PRB1712811 - Persona sync failing
        -   PRB1707248 - Worknotes not added for changes to inbound fields
        -   PRB1698550 - Save button not working on Remote task definition after clone
        -   PRB1711688 - Unable to authenticate due to security updates in December release
-   **Version 1.0.2 - November 2023**

    Service Bridge for Consumers simplifies the interaction between consumers and service providers by offering features like Remote Catalog for seamless service requests and Remote Choice for real-time option selection. It ensures secure and authorized access through Personas and Authorized Users, while Provider Task and Remote Task facilitate transparent and collaborative multi-instance workflows. Additionally, the Transform feature allows both parties to manipulate inbound and outbound data, and makes the whole process flexible and efficient.


