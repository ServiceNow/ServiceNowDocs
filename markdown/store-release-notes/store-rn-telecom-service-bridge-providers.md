---
title: Service Exchange for Providers release notes
description: Version history for the Service Exchange for Providers application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-service-bridge-providers.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 13
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Service Exchange for Providers release notes

Version history for the Service Exchange for Providers application on the ServiceNow Store.

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
    -   Journal Field Framework enhancements
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
-   **Version 2.1.33 - March 2026 \(Zurich\)**

    Service Bridge renamed to Service Exchange

-   **Version 2.0.70 - March 2026 \(Yokohama\)**

    Service Bridge renamed to Service Exchange

-   **Version 2.3.9 - March 2026**
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
        -   Custom URL support: Improved handling and reliability.
        -   Entitlements \(Checkout/Refresh\): No longer deletes existing entitlements when still valid.
        -   Cloning: Variable Sets on the target instance are no longer removed after a clone.
        -   Pre-onboarding guardrail: Added a pre-insert warning on Registration tasks to run the pre-onboarding suite and review the Health Dashboard.
-   **Version 2.2.5 - September 2025**

    Fixed: Provider tasks are showing internal values for remote choice variables in variable sets instead of their display values \(PRB1925091\).

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
        -   Error message appears if the same target field is used twice in one RTD \(PRB1892515\)
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
        -   Data Scope Protection
            -   Adds the ability for ServiceNow internal application teams, like HRSD, to ensure that sensitive data is only accessible to application administrators when data is passed through Service Bridge.
    -   Fixed:
        -   PRB1823044 - Company mismatch preventing some transforms from being executed
        -   PRB1787085 - Not able to sync attachments from provider to consumer using RPS inbound subflow
        -   PRB1782692 - Unable to set new field value when returning null or empty.
-   **Version 2.0.30 - October 2024**
    -   Fixed:
        -   PRB1796564 - \[Provider\] RTD having existing multiple entitlements are removed by the refresh entitlements scheduled job except one random entitlement post upgrade
        -   PRB1800310 - Deletions and status changes of existing configurations need to be sent to consumers on 1.x.x when provider is on 2.x.x
        -   PRB1799772 - Can't Edit Remote Catalog Items after Service Bridge Upgrade
        -   PRB1795471 - Off-board button of Service Bridge 2.0.2 is deleting all variable set
        -   PRB1787307 - Service Bridge Connection breaks after cloning over the instance
-   **Version 2.0.20 - August 2024**
    -   New:
        -   Mismatched version support
            -   Enables providers and consumers to be on different versions of Service Bridge
        -   Configuration Revisions
            -   Adds the ability to upgrade and publish new Remote Record Producers, and Remote Task Definitions without breaking customers that have not upgraded yet.
        -   Maintain RRP GUID between instances
            -   Remote Record Producers are now created with the same sys\_ids on the consumer as on the provider enabling consumers to reliably create processes that reference them.
    -   Changed: Configuration Revisionsis a change to how configurations like RRPs, and RTDs are published and edited. New records are created for each publish to retain existing functionality for consumers that have not yet updated.
    -   Fixed:
        -   PRB1754866 Skipped ACL on Plugin Installation of Service Bridge Base
        -   PRB1724168 Service Bridge : Case reopened from Provider\(SIT\) did not move consumer\(POC\) incident to "In Progress".
        -   PRB1753291 Service Bridge Provider Configuration - Admin user unable to create Provider record
        -   PRB1762834 Service Bridge for Providers application makes "Remote choice display field" mandatory on variables table
        -   PRB1753302 Service Bridge Provider Instance - setting up Flow to trigger incident create from Provider to Consumer throwing errors
-   **Version 1.1.2 - March 2024**
    -   Fixed:
        -   In some instances, the OAuth Cryptographic Module has its access policy set toReject,which will block Service Bridge's ability to complete registration for a consumer.
            -   We added an error message in the Provider instance on the Consumer Registration task with instructions to resolve this issue if it exists.
        -   The Consumer Registration Process would fail to start if a Right-ClickSavewas used instead of clicking theSaveUI Action on the form.
            -   We have changed the solution to ensure the registration process always starts regardless of how the Registration task is inserted.
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
        -   Added Oauth KMF Key Exchange to support updated security controls. This update includes a Retry key exchange request UI Action that appears on the Consumer Registration task if there is any issue with the key exchange.
    -   Fixed:
        -   PRB1712507/PRB1677764 - duplicate attachments
        -   PRB1712811 - Persona sync failing
        -   PRB1707248 - Worknotes not added for changes to inbound fields
        -   PRB1698550 - Save button not working on Remote task definition after clone
        -   PRB1711688 - Unable to authenticate due to security updates in December release
-   **Version 1.0.2 - November 2023**
    -   New Application and transport:
        -   Simplified Experience
        -   No Copy/Paste for onboarding
        -   No manual plugins to install
        -   Register instances in minutes
        -   Improved Transport Layer
        -   REST Webservices
        -   OAUTH2 authentication
        -   Supports On-prem Instances
        -   Requires HTTPS ports to be open for REST webservices
    -   Remote Task Virtual Mappings:
        -   Virtual inbound and outbound field mappings allow fields to be mapped between instances that do not exist on the source table.
    -   Virtual &amp; Global Transforms:
        -   Global Transforms can be created that will run for any connected consumer unless it is overridden at the consumer level.
        -   Virtual Transforms can be created that will run against virtual inbound and outbound fields to set or transform their values
    -   Remote Scratchpad:
        -   Enables name/value pairs to be added to Provider Tasks and Remote Tasks from server side scripts in the provider and consumer instances. These pairs can be used to augment custom processes that flow between instances passing data between the two.
    -   Clone excludes/preserves:
        -   Clone excludes/preserves for Service Bridge are automatically installed with the application. This allows for the connection between instances to survive even if the instances are cloned over.
    -   Renamed Provider Request to Provider Task:
        -   The Provider Task table enables all providers of services using Service Bridge to be transparent and collaborative with their consumers that use ServiceNow.
        -   Provider tasks represent work that is being performed in a provider's ServiceNow instance and monitored in a consumer's instance.
        -   These is no cost to license and no configuration required for the consumers to use this feature, and they can collaborate with all of their providers on this single native table with zero configuration to their instance.
-   **Version 3.2.4 - November 2023 \(Legacy\)**

    Fixed: Various stability fixes around entitlements, attachments, and cross-scope issues.

-   **Version 3.2.0 - May 2023**
    -   New:
        -   Support for Glide List field types in Remote Task mappings
        -   Global transforms added that work across all connected accounts
    -   Changed: Attachments now sync to the parent record of a Remote Task instead of just writing a comment.
-   **Version 3.1.2 - February 2023**
    -   New: Added field dependencies to Remote Choice fields
    -   Changed:
        -   Updated column labels to all use sentence case
        -   Providers can no longer create configurations before completing provider setup
-   **Version 3.1.1 - December 2022**

    Fixed: Domain Separation - Tasks not getting inserted with the correct domain

-   **Version 3.1.0 - November 2022**
    -   New:
        -   Remote Choice- Enables a customer to read the choice list for a reference variable directly from the providers instance. Remote Choice can eliminate the need for many replication-type integrations.
        -   Transform Framework- Enables a provider to transform inbound and outbound data for Remote Task connections with their customers. e.g. simple matching transforms like state-to-state or advanced transforms like converting references to correlated IDs.
    -   Fixed: The Provider task field on the Provider Request table now gets updated on the customer instance for proactive cases.
-   **Version 3.0.0 - August 2022**
    -   New:
        -   Service Bridge: Authorized User: Add and manage user access to create requests and orders from the published items in the service catalog on the customer's ServiceNow instance. This feature also enables the customer to manage the list of users within the criteria provided by the provider from their own instance.
        -   Service Bridge: Remote Task: Resolve and fulfill multiple customer tasks, such as incidents, cases, and service requests. This feature eases the synchronization and configuration of tasks in between the instances of provider and customer. The Remote Task Outbound Assignment enables the sender to provide more relevant information for the incident or case or request. Remote Task Inbound Assignment enables the receiver to take action on the incident or case or request.
    -   Changed:
        -   Only one active group for administrative tasks and automated emails: In previous versions of the Service Bridge application, there were two admin groups, Service Bridge Admins for the automated email notifications and Service Bridge Admin Group for all administrative tasks. Starting with the Tokyo release, the Service Bridge Admins group is removed and all of its users are moved to the group Service Bridge Admin Group. Service Bridge Admin Group has been renamed to Service Bridge Admins. This group is now used to manage both administrative tasks and email notifications.
        -   Creation of cases through a new Service Bridge channel in CSM: Starting with the Tokyo release of Service Bridge, case tasks in the provider's instance are now created with the channel set to Service Bridge instead of eBonding.
-   **Version 2.0.5 - June 2022**

    Fixed: Error that occurred when an incident is created via trouble ticket API.

-   **Version 2.0.4 - May 2022**
    -   Fixed:
        -   Restrict deletion of Remote Record Producer once it is published for customer
        -   Fixed global script include KB link url and changed warning message to provide more information
        -   Changed the provider order/order line item flow action name
-   **Version 2.0.3 - February 2022**
    -   New:
        -   Ability to directly publish remote record producers from one instance to another
        -   Ability to automatically keep items up to date across all customer accounts
-   **Version 1.2.0 - July 2021**

    Changed: Application name changes and bug fixes.

-   **Version 1.1.1 - May 2021**

    Changed: Minor release to remove an internal application dependency.

-   **Version 1.1.0 - March 2021**

    Changed: This release incorporates an update to the new service catalog state model which extends to remote record producers in eBonding applications.

-   **Version 1.0.1 - December 2020**

    Changed: Changes to support Order Management for Telecommunications

-   **Version 1.0.0 - September 2020**

    Enables telecommunications service providers to offer enterprise customers a differentiated service experience by allowing the enterprise customer to consume and monitor provider service delivery from their own IT Service Portal.


**Parent Topic:**[ServiceNow Store - Technology Provider Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

