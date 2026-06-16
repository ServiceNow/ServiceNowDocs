---
title: Sourcing and Procurement Operations Integration with Ariba release notes
description: Version history for the Sourcing and Procurement Operations Integration with Ariba application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-procurement-operations-integration-ariba.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Sourcing and Procurement Operations Integration with Ariba release notes

Version history for the Sourcing and Procurement Operations Integration with Ariba application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.0.1 - June 2026 \(Australia\)**

    Fixed: Implemented Directive DIRS0000421 – Non-Glide Cobalt Raven ACLs in Product Code, along with the corresponding true-up support enhancements.

-   **Version 0.5.1 - June 2026**
    -   New: Introduced support for SAP Ariba REST to create purchase requisitions in SAP Ariba, enabling streamlined sourcing and procurement operations.
    -   Fixed:
        -   Resolved an issue that caused duplicate error tasks to be generated during the Goods Receipt \(GR\) process, ensuring accurate tracking and processing of procurement activities.
        -   Fixed an issue in the Fetch Supplier Bids subflow for Sourcing Events when bids remained un-awarded in SAP Ariba. This improves subflow reliability and data accuracy.
        -   Resolved an issue during Supplier Requisition \(SR\) creation in SAP Ariba that caused Sourcing Events to be retained indefinitely in the In-Process state.
-   **Version 0.4.0 - January 2026**

    New: Added functionality to fetch shipment details from SAP Ariba.

-   **Version 0.3.0 - December 2025**
    -   Changed: Added granular roles to system properties in accordance with new directives.
    -   Fixed:
        -   Removed hard-coded timeout values to improve configurability and system flexibility.
        -   Updated the Quantity field data type from Integer to Decimal in the Sourcing Event in SAP Ariba subflow to ensure accurate numerical precision.
-   **Version 0.2.4 - November 2025**

    Fixed: Minor fixes

-   **Version 0.2.2 - August 2025**

    Fixed: Updated all error messages in the Script include to use gs.getMessage for translation purposes.

-   **Version 0.2.1 - June 2025**

    Minor bug fixes in fetching Awarded Bid's from SAP Ariba Rest to SN.

-   **Version 0.2.0 - March 2025**
    -   Changed:
        -   SAP Ariba REST - Retrieving supplier bids for an event and downloading attachments from supplier responses
        -   SAP Ariba REST - Awarding bid to supplier
-   **Version 0.1.0 - January 2025**
    -   This application provides you with the ability to perform the below operations in Sourcing and Procurement Operations to SAP Ariba:
        -   SAP Ariba REST - Create a goods receipt
        -   SAP Ariba REST - Creation and editing of sourcing events along with products and suppliers

