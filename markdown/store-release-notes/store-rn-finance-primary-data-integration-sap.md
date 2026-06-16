---
title: Primary Data Integration with SAP release notes
description: Version history for the Finance Operations Management Primary Data Integration with SAP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-primary-data-integration-sap.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Primary Data Integration with SAP release notes

Version history for the Finance Operations Management Primary Data Integration with SAP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.0.0 - June 2026 \(Australia\)**

    Fixed: Implemented Directive DIRS0000421 – Non-Glide Cobalt Raven ACLs in Product Code, along with the corresponding true-up support enhancements.

-   **Version 4.8.0 - June 2026**
    -   New:
        -   New directive changes have been implemented for - DIRS0000409 - Invalid Roles in ACLs Directive.
        -   Implemented directive changes for DIRS0000409 – Invalid Roles in ACLs.
    -   Fixed:
        -   Fixed an ERP Source ID issue in the following two subflows, where the ERP Source sys\_id was being populated in the staging table instead of the ERP Source name:
            -   Fetch GL accounts from SAP ECC v2
            -   Fetch FX rate from SAP ECC v2
-   **Version 4.6.2 - March 2026**

    Fixed: Updated the SAP S/4HANA OData \(sn\_hana\_odata\_spk\) spoke-dependent plugin version to support SAP Primary Data Integration \(PDI\) certification.

-   **Version 4.6.0 - January 2026**
    -   New:
        -   Added Security Directive for Read-Only fields.
        -   Added a Fix Script to update the entity name from 'Department' to 'Buyer Groups'.
    -   Changed:
        -   Implemented Read-Only security directives for SAP Primary Data Integration, applying required field-level changes in line with the Read-only field remediation guidelines.
        -   Enabled Purchase Group data retrieval from SAP ECC, SAP OData, and SAP HANA RFC using the updated Buyer Group staging process.
    -   Fixed: Corrected a spelling error in the SAP S4 HANA RFC integration service property for Fetch Payment Term by changing 'qyery' to 'query'.
-   **Version 4.4.0 - December 2025**
    -   Changed: Added granular roles to system properties in accordance with new directives.
    -   Fixed: Removed hard-coded timeout values to improve configurability and system flexibility.
-   **Version 4.3.6 - November 2025**

    Fixed: Minor fixes

-   **Version 4.3.0 - August 2025**

    Fixed: Updated script to reflect gs.getMessage changes - PDI

-   **Version 4.2.6 - May 2025 \(Yokohama\)**

    Minor bug fixes.

-   **Version 4.2.1 - May 2025 \(Xanadu\)**

    Minor bug fixes.

-   **Version 4.2.0 - March 2025**

    Fixed: The ERP source field has been deprecated from the global tables \(cmn\_department, cmn\_cost\_center, cmn\_location,\) prompting updates to redirect ERP source details into a new ERP source mapping table.

-   **Version 4.0.1 - December 2024**
    -   New:
        -   You can now fetch the following entity data from SAP ECC and SAP S4 HANA into ServiceNow:
        -   -   Legal entity
-   Cost center
-   Material
-   Supplier
-   Currencies
-   Conversion rates
-   GL accounts
-   Purchasing organizations
-   Departments
-   **Version 4.0.0 - October 2024**
    -   Built Integration capabilities with SAP ECC and SAP S4 HANA with ServiceNow to perform the following actions on the entities
    -   Fetch the following entity data from SAP ECC and SAP S4 HANA into ServiceNow:
        -   Legal entity
        -   Cost center
        -   Material
        -   Supplier
        -   Currencies
        -   Conversion rates
        -   GL accounts
        -   Purchasing organizations
        -   Departments
    -   All of these have the option to do a full pull or a conditional pull.
-   **Version 3.1.0 - August 2024**
    -   New:
        -   Fetch Cost Centers Stream from SAP S4 HANA Cloud
        -   Fetch GL Accounts in Chart of Accounts SAP S4 HANA Cloud
        -   Fetch services from SAP ECC v2
        -   Fetch plant address from SAP ECC v2
-   **Version 3.0.1 - July 2024**
    -   New:
        -   Fetch Purchasing Group from SAP S4 HANA OData
        -   Fetch Materials from SAP S4 Hana OData
        -   Fetch GL Accounts from SAP S4 HANA OData
        -   Fetch Cost Centers from SAP S4 HANA OData
        -   Fetch Currencies from SAP S4 HANA OData
        -   Fetch Purchasing Organizations from SAP S4 HANA OData
        -   Fetch Legal Entities from SAP S4 HANA OData
        -   Fetch FX Rates from SAP S4 HANA OData
        -   Fetch Payment Terms from SAP S4 HANA OData
        -   Fetch Suppliers from SAP S4 HANA OData
        -   Fetch Plant Addresses from SAP S4 HANA OData
        -   Data retrieval from SAP - Fetch purchasing organizations
        -   Data retrieval from SAP - Fetch purchasing groups
        -   Data retrieval from SAP - Fetch payment terms
        -   Data retrieval from SAP - Fetch Legal Entities
        -   Data retrieval from SAP - Fetch Cost Center
        -   Data retrieval from SAP - Fetch Currencies
        -   Data retrieval from SAP - Fetch GL Accounts
-   **Version 2.0.4 - March 2024**

    Minor fixes.

-   **Version 1.0.1 - July 2023**

    This plugin provides customers with an ability to fetch entity data like legal entity, cost center, material, suppliers etc from SAP ECC and SAP HANA into ServiceNow.


