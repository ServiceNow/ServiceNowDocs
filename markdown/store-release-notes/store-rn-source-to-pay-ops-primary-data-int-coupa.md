---
title: Primary Data Integration with Coupa release notes
description: Version history for the Primary Data Integration with Coupa application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-source-to-pay-ops-primary-data-int-coupa.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Primary Data Integration with Coupa release notes

Version history for the Primary Data Integration with Coupa application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.0 - June 2026 \(Australia\)**
    -   New:
    -   -   Added Fetch chart of accounts subflow in Coupa.
    -   Note: The Account Name and Ledger Account fields populated in the Ledger Accounts \(sn\_fin\_gl\_account\) are a combination of Chart of Account Code:Chart of Account Name.
    -   Changed:
        -   DIRS0000421:
            -   True up changes Non-Glide Cobalt Raven ACLs in Product Code for Coupa PDI Integration \(PDI\).
            -   Updated Non-Glide Cobalt Raven ACLs in Product Code for Primary Data Integration with Coupa
    -   Fixed:
        -   Resolved an issue where the Fetch Purchase Order subflow ran indefinitely and did not mark the integration as failed upon exceptions.
        -   Fixed a defect causing the Fetch Supplier Payment subflow to remain stuck indefinitely \(observed at step 19\).
        -   Corrected behavior where integration service job tracker records were not marked as failed during internal server errors.
        -   Fixed an issue where Coupa fetch subflows continued executing after failure, resulting in infinite execution loops, duplicate data processing, and inconsistent integration states.
-   **Version 3.8.0 - June 2026**
    -   New: Added Fetch Chart of Accounts subflow in Coupa.
    -   Fixed:
        -   Resolved an issue where the Fetch Purchase Order from Coupa subflow ran indefinitely and did not mark integrations as failed on exceptions.
        -   Fixed the Fetch Suppliers Payment from Coupa subflow getting stuck during execution.
        -   Corrected integration service job tracker behavior to ensure failed status is updated for internal server errors.
        -   Prevented infinite loop execution in Coupa fetch subflows after failure, avoiding duplicate processing and inconsistent states.
-   **Version 3.7.0 - March 2026**

    New: Added a Fetch Plant Addresses subflow in Coupa to retrieve plant address details.

-   **Version 3.6.0 - December 2025**

    Changed: Added granular roles to system properties in accordance with new directives.

-   **Version 3.5.0 - August 2025**
    -   New: Added a subflow for Lookup Receipt details from Coupa.
    -   Fixed:
        -   Corrected plugin directory in plugin.xml for ERP Integration in app-coupa-data-int \(internal\).
        -   Updated the Lookup Purchase Order process to ensure the Name field in the COA custom table is unique.
-   **Version 3.0.0 - April 2025**

    New:

    -   Fetch Legal Entity details from Coupa to ServiceNow
    -   Fetch Currency details from Coupa to ServiceNow
    -   Fetch Conversion Rate details from Coupa to ServiceNow
-   **Version 1.0.0 - November 2024**
    -   This application enables integration between the Source-to-Pay Integration Framework and Coupa, allowing you to create and update the following Primary Data:
        -   Legal Entity
        -   Currencies
        -   Conversion Rates

