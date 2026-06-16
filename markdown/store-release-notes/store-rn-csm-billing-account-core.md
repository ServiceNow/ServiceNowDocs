---
title: Billing Account Core release notes
description: Version history for the ServiceNow Billing Account Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-billing-account-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Billing Account Core release notes

Version history for the ServiceNow® Billing Account Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

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

**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

