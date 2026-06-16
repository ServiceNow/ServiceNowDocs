---
title: Customer Service Install Base Management release notes
description: Version history for the Customer Service Install Base Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-customer-service-install-base-mgmt.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Customer Service Install Base Management release notes

Version history for the Customer Service Install Base Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.5.0 - March 2026**
    -   New: Data model changes to support related pricing in sold products.
    -   Added a new field 'Derived price' on the sold product table.
    -   Added a new field 'Contributing sold product' on the sold product pricing adjustments table.
-   **Version 4.4.1 - February 2026**
    -   New: Reference added to support Billing Accounts for sold products.
    -   Changed: Enhanced sold product workflows to honour the start and end dates of the products.
    -   Fixed: Minor defects
-   **Version 4.2.1 - January 2026**

    Changed: Minor security defect fixes and enhancements.

-   **Version 4.1.0 - December 2025**
    -   Changed:
        -   Minor enhancements
            -   Split from and Split from root to track lineage during upsells, downsells, and expiration date changes ensuring accurate order management, compliance, and analytics.
            -   Enables user with feature admin role to manage administrative tasks like read, write, create, delete, data view, and case view related to install base and sold product related entities.
-   **Version 3.2.0 - August 2025**
    -   New:
        -   Support to capture provider service organization and unique identifier on the install base item table
        -   Support to capture pricing information and pricing adjustments on the sold product table
    -   Changed: Support for the base table of install base item on the cmdb model category
    -   Fixed: Minor bug fixes
-   **Version 3.1.2 - June 2025**

    Minor bug fixes.

-   **Version 3.1.0 - May 2025**

    New: Data classifications for install base item and sold product tables.

-   **Version 3.0.0 - February 2025**

    Enables customers to capture the current state of their install base and establish the relationship to any downstream entities that might impact their functioning.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

