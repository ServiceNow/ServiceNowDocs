---
title: GRC: Entity Based Access release notes
description: Version history for the GRC: Entity Based Access application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-entity-based-access.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Entity Based Access release notes

Version history for the GRC: Entity Based Access application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   This release adds new security restrictions, performance improvements, and localization updates to GRC Entity-Based Access.
    -   Audit Workspace restricts sensitive configurations: Access configuration records flagged as audit-relevant are now visible only to users with the Third Line Manager role when Audit Workspace is installed alongside Entity-Based Access, hiding them from general users to enhance audit security.
    -   Row-level query security enforced platform-wide: All Entity-Based Access tables now have platform-managed row-level query restrictions, ensuring that users only see rows they are authorized to access during list views, reports, and REST queries, improving security and performance.
    -   Preservation of custom query ACLs: During plugin installation and upgrades, custom query-level ACLs are detected and preserved by deactivating conflicting platform defaults, ensuring that customer customizations remain intact and clearly distinguished from system-supplied ACLs.
    -   Improved access resolution performance: The process determining user access to parent records has been optimized to deduplicate matching records within the database, resulting in faster list loads and access checks without changing which records users can see.
    -   Tightened authorization on table-label lookup: The internal service that returns display labels for Entity-Based Access reference tables now checks read permissions before providing the label, preventing unauthorized users from seeing table names in the user interface.
    -   Localization updates in 23 languages: Translations for system messages, UI labels, and documentation have been refreshed across 23 languages, improving the experience for non-English speakers and ensuring previously missing strings are now translated.
-   **Version 22.0.1 - March 2026**

    Fixed: Emails are sent upon completion of the bulk utility configurations job to notify users of successful changes or failures.

-   **Version 21.1.4 - December 2025 \(Zurich\)**
    -   New: Record Attributes User Access control: Maintain seamless access for users and groups referenced in record fields even though entity-based access is enabled. This avoids manual configurations, reduces administrative overhead, and helps in adopting entity-based access with minimal disruption.
    -   Fixed: When Entity type configuration is deactivated, Entity type configuration was not removing the EBA restriction.
-   **Version 21.0.2 - August 2025**
    -   New:
        -   Continuous maintenance of access restrictions on entity's related record types.
        -   Introduced "Entity based data access rules" configuration.
            -   Support for enabling Entity-based access on custom tables.
            -   Provided entity-based access admin to perform CRUD operations on "Applicable record type" table.
    -   Changed:
        -   Entity access update utility experience from record page to guided assistance.
        -   Apply entity-based access \(EBA\) restrictions at the record level by using guided assistance in the bulk access update utility.
        -   Guided assistance consists of a four-step process:
            -   Define the scope for the relevant entities, entity types, or entity classes.
            -   Scope the related record types
            -   Apply the conditions to each record type to refine the scope
            -   Review the selected records before you execute and initiate the update
    -   Fixed:
        -   Entity-based access configuration deactivation behaviour
        -   Deactivate entity-based access configuration, enabling the system to automatically assess the records that it impacts.
        -   If only the configuration is restricting a record, the access restrictions are removed.
        -   If other configurations also apply to the record, the restrictions remain in place and only the selected configuration is deactivated.
-   **Version 20.1.4 - May 2025**
    -   New framework to set up configurations to restrict access on entities and related downstream objects.
    -   For example, restrict access to Risks and Controls of specific Locations or Entities to certain User groups or Users.

