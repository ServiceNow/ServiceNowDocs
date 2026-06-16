---
title: Telecommunication Open APIs release notes
description: Version history for the Telecommunication Open APIs application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-telecom-open-apis.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Telecommunications Service Management release notes, ServiceNow Store release notes]
---

# Telecommunication Open APIs release notes

Version history for the Telecommunication Open APIs application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.1.0 - June 2026**
    -   Changed:
        -   TMF 637 - Fixed the Product Inventory Response Structure
        -   TMF 622 - Fixed to Return Display Value Instead of Internal Value for Order Item Characteristic
-   **Version 7.0.0 - March 2026**
    -   Fixed:
        -   Security fixes for sql injection, unescaped json string
        -   Changed the Cancellation logic so that it should not be verifying versions.
-   **Version 6.1.0 - January 2026**
    -   Changed:
        -   Support enrichment flow for orders created via Product and Service order API
        -   Remove Approval step for Inflight Orders created via Product and Service ordering APIs if Auto Approve sys property is true=
    -   Fixed:
        -   Correct the mapping for Recurring Charges in TMF 622 which was incorrectly mapped.
        -   Replace orderRelationship with serviceOrderItemRelationship in case of Service Order API which was incorrectly mapped.
-   **Version 6.0.9 - December 2025**
    -   Includes TM Forum Open APIs for catalog, ordering and inventory management. Key APIs include
        -   TMF 620/633: Catalog Management- Enhanced the existing operations \(GET, LIST, DELETE and PATCH\) to support sending correct version
        -   TMF 622/641: Order Management - Enhanced the existing POST and PATCH operations to support referencing the correct version
        -   TMF 637: Product Inventory Management -  Support PATCH and DELETE operations for Product Inventory
        -   TMF 648: Quote Management - Enhance POST, GET, PATCH and DELETE operations to support Quote with complex characteristics and associate the correct version
-   **Version 5.0.2 - August 2025**
    -   Below new APIs were added:
        -   TMF 632 : Party Management API : Support of POST, GET, LIST, PATCH and DELETE for Party Entities
        -   TMF 648 : Quote Management API : Support of POST, PATCH, GET, LIST and DELETE for Quotes
        -   TMF 697 : Work Order Management API : Support of POST, PATCH , GET, LIST and DELETE for Work Orders
    -   Below APIs were updated:
        -   TMF 620/TMF622/TMF641/TMF 633 : Support for Complex Characteristics
-   **Version 4.1.0 - May 2025**
    -   Changed:
        -   TMF 620: Improved the POST, PATCH, GET and LIST operations to for Bundled offers as well as supporting additional attributes \(isSellable, relationship type, lifecycle status etc.\)
        -   TMF-622: Improved the POST, PATCH, GET and LIST operations to support Bundled Offers for Product Order
        -   TMF-637: Improved the POST, PATCH, GET and LIST operations to support Bundled Offers for Product Inventory
-   **Version 4.0.0 - February 2025**
    -   Added the product offering price APIs to the product catalog open API.
    -   GET: api/sn\_tmf\_api/catalogmanagement/productOfferingPrice/\{id\}
    -   LIST: api/sn\_tmf\_api/catalogmanagement/productOfferingPrice
    -   POST: api/sn\_tmf\_api/catalogmanagement/productOfferingPrice
    -   PATCH: api/sn\_tmf\_api/catalogmanagement/productOfferingPrice/\{id\}
    -   DELETE: api/sn\_tmf\_api/catalogmanagement/productOfferingPrice/\{id\}
-   **Version 3.1.0 - November 2024**

    New: PATCH appointment API, GET/LIST appointment API, DELETE appointment API.

-   **Version 2.1.0 - August 2024**
    -   TMF 641 Service Order changes as per TMF documentation for certification
    -   TMF 620 catalog changes related to conformance
    -   TMF 639 resource inventory changes
-   **Version 2.0.0 - February 2024**
    -   New:
        -   Product offering Category API support
        -   Consumer order support
    -   Changed: Product Offering API changes to accept category information
    -   Fixed: Date format issue fixed in API response
-   **Version 1.0.0 - November 2023**

    Includes TM Forum Open API and related functionality.


**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

