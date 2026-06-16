---
title: SAP S4 HANA OData Spoke release notes
description: Version history for the SAP S4 HANA OData Spoke application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-sap-s4-hana-odata-spoke.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# SAP S4 HANA OData Spoke release notes

Version history for the SAP S4 HANA OData Spoke application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.12.0 - June 2026**

    Security patch for non-glide ACLs

-   **Version 1.11.2 - May 2026**

    Added an optional field of "Purchase Order" under Create Service Goods Receipt Action--&gt;ServiceEntrySheetItem

-   **Version 1.11.1 - March 2026**
    -   Created Line Item on Existing Purchase Order - Added an input child property "OrderQuantityUnit" in the \_PurOrdAccountAssignment object and "ScheduleLineDeliveryDate" field.
    -   Created Purchase Order - Added new field "ScheduleLineDeliveryDate" field under "Purchase\_Order\_Schedule\_Line" and PurOrdAccountAssignment&gt;&gt;OrderQuantityUnit
-   **Version 1.11.0 - December 2025**
    -   Enhanced 6 actions from OData v2 to OData v4:
        -   Update Purchase Order for ASN
        -   Cancel Purchase Order Line
        -   Create Line Item on Existing Purchase Order
        -   Create Purchase Order
        -   Update Purchase Order
        -   Update Purchase Order Line
-   **Version 1.10.0 - October 2025**
    -   Converted the following Look up Purchase Orders Stream action from OData v2 to OData v4
    -   Added 7 new Spoke Actions
-   **Version 1.9.0 - December 2024**

    Added 6 more spoke actions.

-   **Version 1.8.0 - November 2024**

    Added: More input/output fields for Create Goods Receipt, Look up Invoices, Create Supplier, Create Invoice, and Create Non-PO Invoice actions.

-   **Version 1.7.0 - September 2024**

    Added more output fields for the existing 3 actions: Create Supplier, Create Invoice, and Look Up Invoices Stream.

-   **Version 1.6.0 - August 2024**

    Added 3 more actions.

-   **Version 1.5.0 - June 2024**

    Added 5 actions.

-   **Version 1.4.1 - May 2024**

    Added 4 actions.

-   **Version 1.3.0 - April 2024**

    Added 7 actions.

-   **Version 1.2.0 - January 2024**

    Added 5 actions, 1 remote table, 1 sample outbound flow, and 1 sample inbound flow.

-   **Version 1.1.0 - December 2023**

    Added 5 more actions.

-   **Version 1.0.0 - November 2023**
    -   SAP S/4 HANA OData spoke is built by Bristlecone Inc.
    -   SAP S/4 HANA Odata spoke provides a list of actions that interact with SAP standard OData APIs. It provides the foundation to synchronize ServiceNow and SAP S/4 HANA, such as looking up suppliers, materials, purchase groups, COAs, curriencies, business partner addresses, and so on.
    -   Given that SAP S/4 HANA is a highly customizable system, SAP S/4 HANA OData Spoke also showcases the design pattern that can support custom OData APIs and more standard OData APIs beyond what is out of the box.
    -   When both ServiceNow and SAP S/4 HANA do financial operations together, the possibilities are endless.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

