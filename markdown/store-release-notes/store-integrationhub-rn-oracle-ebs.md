---
title: Oracle EBS spoke release notes
description: Version history for the Integration Hub Oracle EBS Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-oracle-ebs.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Oracle EBS spoke release notes

Version history for the Integration Hub Oracle EBS Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.14.0 - June 2026**

    Security patch on non-glide ACLs

-   **Version 1.13.4 - April 2026**

    Fixed: variable name now matches with the input variable org\_id at the preprocessing script of the Submit Blanket Release - Run Concurrent Program

-   **Version 1.13.2 - July 2025**
    -   Fixed:
        -   Data types of Quantity field to number for 7 actions
            -   Create/update Purchase Order
            -   Create Blanket Release
            -   Create AP Invoice
            -   Create PO Goods Receipt
            -   Create/update Blank Purchase Agreement
        -   Security patch update
-   **Version 1.13.0 - November 2024**

    Evaluated sandbox access for client-callable script includes and marked sandbox callable as false.

-   **Version 1.11.3 - October 2024**
    1.  Added the attribute "agreed\_amount" to the action Create Blanket Purchase Agreement.
    2.  Included Ship to Location ID for the non-PO invoices from the Create Invoice Action.
-   **Version 1.11.2 - September 2024**
    -   Added sample subflow on fetching AP invoice details.
    -   Added more input and output fields for 9 actions.
        -   Create PO
        -   Update PO
        -   Cancel PO
        -   Create Blanket Purchase Agreement
        -   Update Blanket Purchase Agreement
        -   Create Blanket Release
        -   Create Goods Receipt
        -   Cancel Goods Receipt
        -   Create Invoice
    -   Added a more user-friendly message for the "Look up" actions.
-   **Version 1.10.1 - July 2024**
    -   Fixed:
        -   Providing more accurate error messages on HTTP status code = 200 errors.
        -   Order of inputs requires change in the Create Blanket Release and Update Blanket Release Actions.
-   **Version 1.10.0 - June 2024**

    Added 13 more actions.

-   **Version 1.9.1 - May 2024**

    Added or updated 17 actions.

-   **Version 1.8.0 - April 2024**

    Added and updated 21 actions total.

-   **Version 1.7.0 - March 2024**

    Added 9 actions.

-   **Version 1.6.0 - February 2024**

    Added support for the additional attribute \(that is, Attribute1 to Attribute15\) fields in the Create Goods Receipt action.

-   **Version 1.5.0 - September 2023**
    -   Fixed:
        -   Continue variable is not found error is displaying while executing Lookup Actions
        -   'licensable' field set to be true in plugin.xml
-   **Version 1.4.1 - September 2022**

    Patch version of Oracle EBS Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.4.0 - December 2021**

    New: Added Create and Look up Transfer Orders Action

-   **Version 1.3.0 - July 2021**

    Added a new customer service management action.

-   **Version 1.2.0 - June 2021**
    -   Added four new sample subflows to showcase how to use the popular actions of:
        -   Create purchase order and purchase order lines
        -   Create goods receipt
        -   Create invoice and invoice lines
        -   Create fixed assets
-   **Version 1.0.1 - May 2021**
    -   New: The Oracle EBS spoke provides a list of modernized REST and JSON actions to interact with the Oracle EBS application. Since Oracle EBS is the gospel of truth for the core Financial and Procurement information, ServiceNow, as the System of Engagement and Action, needs the latest and greatest foundational data to perform subsequent financial-related and so on. This spoke can look up the foundational data, such as cost centers, legal entities, vendor sites, and so on. It can then facilitate popular financial transactions, such as create, update, or cancel purchase order, create goods receipts, look up advance shipment notices, and so on.
    -   Customers can expand the spoke to support almost any records available in Oracle EBS. Dynamic introspection allows customers to preview what fields are available in each record conveniently in Flow Designer.
    -   When both ServiceNow and Oracle do procurement and finance together, the possibilities are endless.

