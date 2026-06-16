---
title: Primary Data Integration with Oracle release notes
description: Version history for the Primary Data Integration with Oracle application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-primary-data-integration-oracle.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Primary Data Integration with Oracle release notes

Version history for the Primary Data Integration with Oracle application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.0 - June 2026 \(Australia\)**
    -   Fixed:
        -   DIRS0000416: Enhanced security by disabling user-supplied JavaScript in the guest sandbox for Primary Data Integration with Oracle.
        -   DIRS0000421:
            -   Implemented Non-Glide Cobalt Raven ACLs within the product code for Primary Data Integration with Oracle.
            -   Aligned and completed \(“true-up”\) related changes to ensure consistent ACL behavior across Oracle PDI components.
        -   Resolved an issue where job tracker records were not updated to a failed state when an internal server error or similar error class occurred. The following Oracle EBS subflows were affected:
            -   Fetch Currencies from Oracle EBS service
            -   Fetch Payment terms from Oracle EBS service
            -   Fetch Plant address from Oracle EBS service
            -   Fetch Purchasing organizations from Oracle EBS service
            -   Fetch FX rates from Oracle EBS service
            -   Fetch Legal entities from Oracle EBS service
            -   Fetch Purchase groups from Oracle EBS service
-   **Version 1.5.0 - June 2026**
    -   Fixed:
        -   DIRS0000416 — Disabled user-supplied JavaScript in the Guest Sandbox for Primary Data Integration with Oracle.
        -   Resolved an issue where job tracker records were not updated to a failed state when an internal server error or similar error class occurred. The following Oracle EBS subflows were affected:
            -   Fetch Currencies from Oracle EBS service
            -   Fetch Payment Terms from Oracle EBS service
            -   Fetch Plant Address from Oracle EBS service
            -   Fetch Purchasing Organizations from Oracle EBS service
            -   Fetch FX Rates from Oracle EBS service
            -   Fetch Legal Entities from Oracle EBS service
            -   Fetch Purchase Groups from Oracle EBS service
-   **Version 1.4.0 - December 2025**

    Changed: Added granular roles to system properties in accordance with new directives.

-   **Version 1.3.0 - August 2025**
    -   Fixed:
        -   All error messages in the script have been updated to use gs.getMessage for translation purposes.
        -   The ERP Source field in ERP Source Configuration has been updated with the correct ERP Source record for Oracle.
-   **Version 1.2.0 - October 2024**
    -   Built Integration capabilities with Oracle EBS and ServiceNow to perform the following actions on the entities:
        -   Look up and pull currencies
        -   Look up Purchasing Org
        -   Look up Purchase Group
        -   Look up Plant Address
    -   All of these have the option to do a full pull or a conditional pull.
-   **Version 1.1.1 - August 2024**
    -   New:
        -   Fetch Inventory Items
        -   Custom Table implementation for Username and Responsibility Implementation
        -   Operating Unit Primary Data Implementation
        -   Fetch Suppliers Subflow - External Unique Id mapping in the table: sn\_fcms\_intg\_office\_location\_stage and Bank Identification Number mapping in the table: sn\_fcms\_intg\_supplier\_payment\_inbound\_stage
-   **Version 1.0.1 - July 2024**

    This application provides customers the ability to fetch entity data like legal entity, cost center, GL accounts, Conversion Rates, Currencies, Purchasing Org, Purchasing Group, Payment Terms, Plant address, Supplier from Oracle EBS into ServiceNow.


