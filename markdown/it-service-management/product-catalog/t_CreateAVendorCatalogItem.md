---
title: Create a vendor catalog item
description: Create a vendor catalog item to associate product models with a vendor.
locale: en-US
release: zurich
product: Product Catalog
classification: product-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Vendor catalog items, Product Catalog, Asset Management, IT Service Management]
---

# Create a vendor catalog item

Create a vendor catalog item to associate product models with a vendor.

## Before you begin

Role required: model\_manager

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Catalog Definition** &gt; **Vendor Items**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the item is built from information in the **Product Model**, **Vendor**, and **Product ID** fields.|
    |Vendor|The supplier that provides the item.|
    |Product model|The specific version or configuration of the item.|
    |Out of stock|The option that indicates whether the item is unavailable for order. This field is important if you are [sourcing request items](../../procurement/concept/c_SourcingRequestItems.md). Clear this check box if the item is available to order.|
    |Product ID|The item identification number assigned by your organization.|
    |List price|The price at which the item retails, excluding vendor discounts.|
    |Vendor price|The price at which the item is available in the vendor catalog. If the vendor offers a discount, the vendor price reflects the discounted price.|
    |Rank tier|Displays the overall ranking for this vendor's products and services, such as Valued Partner or Tactical Supplier. Rank tier expresses your organization's opinion of this vendor's performance. It can be used to decide if the vendor's products should be promoted or discontinued. Users with the vendor\_manager role can edit this field.|
    |Short description|A brief description of the item.|
    |General section|
    |Product catalog item|Name of the product catalog item, if the item has been added to the product catalog. Leave this field empty if you are going to link a vendor catalog item to the hardware catalog.|
    |UPC|The barcode number used to uniquely identify and track items for sale.|
    |Active|Select the check box to list the item in the vendor catalog. Clear this check box to hide the item in the vendor catalog.|
    |Description|A detailed description of the item.|
    |Information section|
    |Specifications|Facts about the item such as size, weight, version, or speed.|
    |Features|Distinct properties or distinguishing characteristics of the item.|

4.  Click **Submit**.


-   **[Link an item to the hardware catalog](t_LinkAnItemToTheHardwareCatalog.md)**  
After you create a vendor catalog item, link the item to the hardware catalog for viewing.
-   **[Link an item to the software catalog](t_LinkAnItemToTheSoftwareCatalog.md)**  
After you create a vendor catalog item, link the item to the software catalog for viewing.
-   **[Publish an item to the hardware catalog](t_PublishAnItemToTheHardwareCatalog.md)**  
After you create a hardware item for the vendor catalog, publish it to the hardware catalog for viewing. The hardware catalog is a section within the service catalog.
-   **[Publish an item to the software catalog](t_PublishAnItemToTheSoftwareCatalog.md)**  
After you create a software item for the vendor catalog, publish it to the software catalog for viewing. The software catalog is a section within the service catalog.

**Parent Topic:**[Vendor catalog items](../concept/c_ManageVendorCatalogItems.md)

**Related topics**  


[Synchronize information](../concept/c_SynchronizeInformation.md)

[View a vendor list](t_ViewAVendorList.md)

