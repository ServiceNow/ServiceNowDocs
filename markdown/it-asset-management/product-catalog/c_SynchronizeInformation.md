---
title: Synchronize information
description: Certain information is synchronized between models, product catalog items, and vendor catalog items.
locale: en-US
release: zurich
product: Product Catalog
classification: product-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Vendor catalog items, Product Catalog, IT Asset Management]
---

# Synchronize information

Certain information is synchronized between models, product catalog items, and vendor catalog items.

When working with models, product catalog items, and vendor catalog items, keep the following in mind:

-   Changes to model record update vendor catalog items automatically only if the vendor catalog items are published, not linked.
-   If a model is linked to a vendor catalog item, any changes to the model do not update the vendor catalog item.
-   After publishing a vendor catalog item or model to the hardware or software catalog, some fields become read-only on the vendor catalog item or product catalog item record. Information can only be updated on the model record.

List of synchronized fields:

-   Description
-   Short description
-   Name
-   Product ID
-   Price
-   Vendor
-   Specs
-   Features
-   Model
-   UPC
-   Model number
-   Cost
-   Manufacturer

**Parent Topic:**[Vendor catalog items](c_ManageVendorCatalogItems.md)

**Related topics**  


[Create a vendor catalog item](../task/t_CreateAVendorCatalogItem.md)

[View a vendor list](../task/t_ViewAVendorList.md)

