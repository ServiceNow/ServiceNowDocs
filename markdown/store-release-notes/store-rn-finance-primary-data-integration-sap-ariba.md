---
title: Primary Data Integration with SAP Ariba release notes
description: Version history for the Primary Data Integration with SAP Ariba application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-primary-data-integration-sap-ariba.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Primary Data Integration with SAP Ariba release notes

Version history for the Primary Data Integration with SAP Ariba application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.1 - June 2026**

    Fixed: Resolved an issue where the ERP source field was missing on the ERP Source Configuration record after app installation.

-   **Version 1.5.0 - January 2026**
    -   Changed:
        -   Enabled Purchase Group data retrieval from SAP Ariba using the updated Buyer Group staging process.
        -   Updated entity naming convention from "Department" to "Buyer Groups" for improved standardization.
-   **Version 1.4.0 - December 2025**

    Changed: Added Granular Roles to the system properties as per the new directives.

-   **Version 1.3.1 - October 2025**

    Changed: Added a flow to fetch Goods Receipts from SAP Ariba.

-   **Version 1.2.1 - March 2025**

    Fixed: Organization Mapping is unavailable in the Supplier Contact Inbound table \(sn\_fcms\_intg\_supplier\_contact\_inbound\).

-   **Version 1.2.0 - January 2025**
    -   New:
        -   You can fetch the following entity data from SAP Ariba into ServiceNow:
            -   Legal entity
            -   Cost Center
            -   FX Rates
            -   Currencies
            -   Purchasing organization
            -   GL Account
-   **Version 1.1.1 - December 2024**
    -   New:
        -   You can now fetch the following entity data from SAP Ariba into ServiceNow:
        -   -   Legal entity
-   Cost Center
-   FX Rates
-   Currencies
-   Purchasing organization
-   GL Account
-   **Version 1.1.0 - August 2024**
    -   New:
        -   Fetch purchase group from SAP Ariba REST
        -   Fetch payment terms from SAP Ariba REST
        -   Minor fixes
-   **Version 1.0.1 - July 2024**

    This application provides customers the ability to fetch entity data like legal entity, cost center, currencies, and purchasing, and so on, from SAP Ariba into ServiceNow.


