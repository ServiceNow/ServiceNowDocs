---
title: Billing Account Core release notes
description: Version history for the ServiceNow Billing Account Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-billing-account-core.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Customer Service Management version history release notes, ServiceNow Store version history release notes]
---

# Billing Account Core release notes

Version history for the ServiceNow® Billing Account Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 3.0.0 - September 2026**
    -   New:
        -   Billing account address
            -   Associate one or more locations with a billing account using the newBilling Account Address table. Each record links a billing account to a location and identifies the address type, and you can mark one address as the primary.
        -   Billing account payment profile
            -   Define how a billing account is paid using the newBilling Account Payment Profile table, which captures the payment method and related payment details for the account.
        -   Payment responsibility on billing accounts
            -   Specify who pays for a billing account with the new Paying party and Paying billing account fields, supporting self, parent, and designated-account payment relationships.
        -   Billing schedules on billing accounts
            -   Schedule when billing occurs for a billing account with the new Billing Schedule field, which links the account to a platform schedule and its schedule entry records. The new billing account schedule viewer \[sn\_billing\_account.schedule\_viewer\] and writer \[sn\_billing\_account.schedule\_writer\] roles control read and write access to these schedules.
    -   Changed:
        -   Billing account roles and responsibility access
            -   Updated the billing account platform roles and CRM billing account granular roles, and registered billing account address, billing account payment profile, and billing schedule \(schedule and schedule entry\) as accessible entities in the responsibility framework.
-   **Version 2.3.4 - August 2026**
    -   New:
        -   Billing Account hierarchy visualization is now available in the Platform \(UI16\) form. Users can view and navigate parent-child relationships directly from the Billing Account form, with interactive expand/collapse and drill-down navigation to related accounts.
        -   Billing Account Type is now auto-populated based on the source customer. When creating a billing account from an Account or Consumer record, the system automatically sets the Billing Account Type according to the source, reducing manual input and ensuring consistency. Users can edit the type before saving.
        -   Default Billing Account view now dynamically displays relevant fields based on the selected Billing Account Type. Admins see Account, Contact, and Consumer fields in the Default view for applicable types, aligning field visibility with Case and Workspace views.
    -   Changed: The CAM user role is no longer required for CRM Billing Account B2B and B2C viewer roles, resolving the subscription issues from earlier versions.
-   **Version 1.0.3 - August 2026**

    New: CAM user role is no longer contained in the Billing Account CRM B2B and B2C viewer roles.- Access to the related party configuration and responsibility definition tables are now driven directly through the CRM Billing Account granular roles.

-   **Version 2.2.0 - June 2026**
    -   Fixed: The sn\_billing\_account.ws\_integration and sn\_billing\_account.viewerroles are now correctly scoped on the billing account records. These roles previously had unintended field-level visibility through a CSM-related ACL.
    -   Removed: The flat Sales Products \(SP\) and Product Inventory \(PI\) related lists on the account's record page on the workspace are replaced by new hierarchical related lists for SP and PI. The underlying SP and PI data is unchanged; only the workspace view configuration is updated, and no other workspace components are affected.
-   **Version 2.1.0 - April 2026**

    Fixed: Fixed defects.

-   **Version 1.0.2 - April 2026**

    Fixed: Security fixes.

-   **Version 2.0.3 - March 2026**

    New: Enhanced the Billing Accounts data model to allow Contacts and Consumers to access Billing Accounts through the Related Parties framework. Access is governed using out-of-the-box system responsibilities and roles, enabling controlled and flexible access management.

-   **Version 1.0.0 - February 2026**
    -   Billing Account Core provides a foundational data model for managing billing accounts across organizations and users. It enables businesses to define, organize, and maintain billing relationships, supporting accurate billing, payments, and scalable financial operations.
    -   The application acts as a central source of truth for billing account data, enabling seamless association with products, invoices, cases, and other related financial entities to deliver complete financial context.

**Parent Topic:**[ServiceNow Store - Customer Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

