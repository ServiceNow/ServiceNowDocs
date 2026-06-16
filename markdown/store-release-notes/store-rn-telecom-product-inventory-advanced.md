---
title: Product Inventory Advanced release notes
description: Version history for the Product Inventory Advanced application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-product-inventory-advanced.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Product Inventory Advanced release notes

Version history for the Product Inventory Advanced application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.1 - June 2026 \(Australia\)**

    Fixed: Minor security fixes

-   **Version 13.0.1 - June 2026 \(Zurich\)**

    Fixed: Minor security fixes

-   **Version 12.1.0 - April 2026**

    This release includes repackaging of files to conform with platform guidelines.

-   **Version 12.0.0 - March 2026 \(Yokohama\)**

    New: Propagating new pricing fields for supporting the delta pricing capability

-   **Version 11.0.2 - January 2026 \(Yokohama\)**

    Fixed minor defects.

-   **Version 11.0.0 - December 2025 \(Zurich\)**

    Providing a mapping between the delta pricing columns

-   **Version 9.3.0 - August 2025**

    Fixed: Localization fix.

-   **Version 8.2.0 - July 2025**

    Added List view for Product Inventory in Business portal.

-   **Version 8.1.0 - May 2025**

    Enabled the customer personas to directly access the Product Inventory using the Business portal by providing the list view.

-   **Version 7.4.0 - February 2025**
    -   Added Specification Class column to product inventory related list to enable users to identify the specification type of the PI
    -   Enabled pricing and subscription fields configuration on Product inventory entity definitions
-   **Version 7.2.0 - November 2024**

    New: Product Inventory MACD: Modify, Disconnect, Suspend and Resume, Create quote from Product Inventory​. With this release, enterprises now have access to product inventory data from the customer account page via a related list. From this list, MACD flows can be initiated to create change orders or quotes for product reconfiguration or DSR \(disconnect, suspend, resume\) activities.

-   **Version 7.1.1 - August 2024**
    -   New: Product Inventory related changes to support creation and fulfillment of product offer bundles with spec/spec hierarchy
    -   Changed: Changes to support TMF 637 API: realizingService is updated to array of objects in the schema
-   **Version 7.0.1 - May 2024**

    Changed: Adding the capability to update product inventory when product spec is updated and a new version rolled out through API.

-   **Version 6.0.0 - February 2024**
    -   New:
        -   Pricing related changes
        -   Support Configuration UI functionality
    -   Fixed: External ID related issue fixed
-   **Version 5.0.0 - November 2023**
    -   New:
        -   Move API code to the new telecommunications application \(sn\_om\_tmt\)
        -   Ingest service order with external product inventory id in related item object and add external id for related item view in platform and workspace
    -   Fixed: Fix included to support parent order line with no-change action with child order line item with suspend action
-   **Version 4.0.0 - August 2023**
    -   New:
        -   TMF641 Service Order Spoke \(Southbound Actions\)
        -   Support External inventory ID in order
        -   Support suspend and restore action for product and service order
        -   Cancel child domain orders when parent domain order is cancelled manually
-   **Version 3.0.0 - February 2023**
    -   Changed: Internal optimization to align to NOW engineering standards
    -   Fixed: Resolved various reported issues.
-   **Version 2.0.1 - November 2022**
    -   Changed: Internal optimization to align to NOW engineering standards
    -   Fixed: Resolved various reported issues.
-   **Version 2.0.0 - August 2022**

    New: Supports catalog versioning and horizontal relationships for product inventory

-   **Version 1.0.1 - June 2022**

    Changed: Updated to account for address relationship change by horizontal OM team.

-   **Version 1.0.0 - February 2022**

    Product Inventory Advanced introduces a product inventory and product characteristics tables to store instances of products that have been delivered to customers, and an API called the Product Inventory Open API to allow product inventory to be created or retrieved programmatically.


**Parent Topic:**[ServiceNow Store - Technology Provider Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

