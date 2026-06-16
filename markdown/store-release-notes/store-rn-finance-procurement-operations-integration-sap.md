---
title: Sourcing and Procurement Operations Integration with SAP release notes
description: Version history for the Finance Operations Management Sourcing and Procurement Operations Integration with SAP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-procurement-operations-integration-sap.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Sourcing and Procurement Operations Integration with SAP release notes

Version history for the Finance Operations Management Sourcing and Procurement Operations Integration with SAP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.0 - June 2026**

    Fixed: Implemented Directive DIRS0000421 – Non-Glide Cobalt Raven ACLs in Product Code, along with the corresponding true-up support enhancements.

-   **Version 2.2.6 - June 2026**
    -   Fixed: Addressed HANA integration issues by restoring the missing Update Purchase Order HANA IDoc subflow.
    -   Changed: Enhanced the Create Goods Receipt \(GR\) use case by mapping Purchase Order details at the item level to support the Create Service Goods Receipt action in SAP HANA.
-   **Version 2.2.4 - March 2026**
    -   Fixed:
        -   Removed unnecessary log entries as part of code cleanup.
        -   Replaced Purchase Order V2 actions with V4 actions.
        -   Resolved Create and Update Purchase Order failures for SAP ECC and HANA IDOC integrations caused by missing Buyer Group \(Purchase Group\) mapping in PO header actions.
        -   Added the missing cross-scope file for the SPO application.
-   **Version 2.2.0 - December 2025**
    -   New: Added Cancel Goods Receipt subflow.
    -   Changed: Added granular roles to system properties in accordance with new directives.
    -   Fixed: Removed hard-coded timeout values to improve configurability and system flexibility.
-   **Version 2.1.16 - November 2025**

    Fixed: Minor fixes

-   **Version 2.1.14 - August 2025**

    Fixed: "Look up Materials by Plants" was added to the "Fetch Materials in Hana RFC" subflow, replacing the deprecated action caused by field data type changes.

-   **Version 2.1.12 - June 2025 \(Yokohama\)**

    Fixed: When a user initiates a partial return of a purchased quantity, an additional purchase order record is automatically created in the outbound table.

-   **Version 2.1.8 - June 2025 \(Xanadu\)**

    Fixed: Minor UI bugs were present when submitting Purchase Orders and Good Receipts.

-   **Version 2.1.6 - May 2025 \(Yokohama\)**

    Minor bug fixes.

-   **Version 2.1.1 - May 2025 \(Xanadu\)**

    Minor bug fixes.

-   **Version 2.1.0 - March 2025**

    Fixed: The ERP source field has been deprecated from the global tables \(cmdb\_model and cmdb\_service\_product\_model\), prompting updates to redirect ERP source details into a new ERP source mapping table.

-   **Version 2.0.7 - January 2025**
    -   New:
        -   The following Sourcing and Procurement Operations objects can be sent both synchronously and asynchronously to SAP ECC and SAP S4 HANA:
            -   Purchase orders
            -   Updates to purchase orders, including cancel purchase orders
            -   Purchase orders with handling fees
            -   Blanket purchase orders
            -   Purchase requisition lines are split across cost centers, custom delivery addresses, and standard delivery addresses
            -   Receipts
            -   Returns
-   **Version 2.0.6 - December 2024**
    -   New:
        -   Enables the Outbound flow of the following Procurement Operations objects both synchronously and asynchronously to SAP ECC and SAP S4 HANA:
            -   Purchase orders
            -   Updates to purchase orders, including cancel purchase orders
            -   Purchase orders with handling fees
            -   Blanket purchase orders
            -   Purchase requisition lines are split across cost centers, custom delivery addresses, and standard delivery addresses.
            -   Receipts
            -   Returns
-   **Version 2.0.5 - October 2024**
    -   Built Integration capabilities with SAP ECC and SAP S4 HANA with ServiceNow to perform the following actions on the entities.
    -   The following Sourcing and Procurement Operations objects can be sent both synchronously and asynchronously to SAP ECC and SAP S4 HANA:
        -   Purchase orders
        -   Updates to purchase orders, including cancel purchase orders
        -   Purchase orders with handling fees
        -   Blanket purchase orders
        -   Purchase requisition lines split across cost centers, custom delivery addresses, and standard delivery addresses
        -   Receipts
        -   Returns
-   **Version 1.4.0 - August 2024**

    Minor fixes.

-   **Version 1.3.0 - July 2024**

    New subflows created for data retrieval from SAP ECC - Sourcing - to Fetch Materials.

-   **Version 1.2.1 - January 2024**

    New: Resubmit for errored records is now available in the respective plugins.

-   **Version 1.2.0 - December 2023**

    New: IDOC now handles updates to purchase order and goods receipt.

-   **Version 1.1.1 - October 2023**

    New: Ability to integrate using SAP IDOC connectors.

-   **Version 1.0.0 - July 2023**

    This application provides you with the ability to send purchase orders, receipts, and returns created in Sourcing and Procurement Operations to SAP ECC and SAP S4 HANA.


