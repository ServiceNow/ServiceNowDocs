---
title: Sales Cart release notes
description: Version history for the Sales Cart application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-sales-cart.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management release notes, ServiceNow Store release notes]
---

# Sales Cart release notes

Version history for the Sales Cart application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.1 - June 2026 \(Australia\)**

    Fixed: Enhanced security by introducing query range ACLs.

-   **Version 2.3.0 - June 2026 \(Zurich\)**

    Fixed: Enhanced security by introducing query range ACLs.

-   **Version 2.1.3 - March 2026 \(Zurich\)**

    New: The term\_month attribute is now mapped from the Sales Cart \[sn\_sales\_cart\] to term\_month in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.

-   **Version 2.1.2 - January 2026 \(Yokohama\)**

    Changed: Corrected currency field population on cart and cart entities for currencies such as Israeli Shekel.

-   **Version 2.1.0 - December 2025 \(Zurich\)**
    -   Changed:
        -   ReplacedBack to Catalog button withRequest for Quote on the Cart page. Previously, theBack to Catalog button enabled you to go back to the catalog to browse more products. TheRequest for Quote button now enables you to initiate RFQs directly from the cart. You can navigate to the catalog using the breadcrumbs.
        -   Updated specific fields in Sales Cart and Sales Cart Line Items tables fromread\_only tostrict\_read\_only for added security.
-   **Version 1.0.0 - August 2025**
    -   Sales Cart enables your business-to-business \(B2B\) customers to:
        -   Create a cart and add product offerings to cart lines
        -   Download a cart
        -   Delete a cart
        -   Create an order from a cart as part of the cart checkout process

**Parent Topic:**[ServiceNow Store - Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-sales-order-management-highlights.md)

