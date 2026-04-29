---
title: Configure Classic Mobile devices
description: When you configure Service Catalog on a Classic Mobile device, you can define the layout and presentation of catalogs. You can then perform actions such as ordering products and services, submit incidents and problems using record producers.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Classic Mobile devices

When you configure Service Catalog on a Classic Mobile device, you can define the layout and presentation of catalogs. You can then perform actions such as ordering products and services, submit incidents and problems using record producers.

## Before you begin

**Important:**

Mobile Classic Is Deprecated!

The App Has Been Removed From The Stores And Can No Longer Be Activated. We Are Not Offering Enhancements, Bug Fixes, Or Support For The App. See [ServiceNow Classic Mobile App Deprecation Effective September 15, 2022](https://community.servicenow.com/community?id=community_article&sys_id=8fd41156db9c3c106064eeb5ca961989).

Role required: admin

## About this task

Users can access the service catalog on Classic Mobile devices to:

-   View and order products and services.
-   Submit incidents and problems using record producers.

**Note:** Users cannot access order guides, wizards, or content items from Classic Mobile devices.

Administrators and catalog administrators can configure the layout, presentation, and other aspects of the service catalog for Classic Mobile devices.

Including:

-   Defining rendering options for Classic Mobile categories.
-   Defining rendering options for Classic Mobile catalog items.

Accessing the Service Catalogon Mobile Devices

To access the service catalog, navigate to **Self-Service** &gt; **Catalog**.

![Screenshot for Service Catalog Classic Mobile homepage.](../image/ServiceCatalogHomepageMobile.png "Service Catalog homepage Classic Mobile")

Catalog items are grouped into categories, which can also contain one or more subcategories.

You can browse and select an item. To browse for an item within a category, tap the category filter to select the category or subcategory.

![Screenshot for Service Catalog category.](../image/MobileUIServiceCatalogCategory.png "Sample service catalog category")

To request an item:

## Procedure

1.  Select an item.

    ![Screenshot for order item Classic Mobile.](../image/OrderItemMobile.png "Order Item Classic Mobile")

2.  Tap any field with an arrow \(&gt;\) to add information, such as the name or location of the requestor, the need-by date, or item quantity.

3.  Tap **Add to Cart** to add the item to your cart. The order screen appears.

    ![Screenshot for Order Item Classic Mobile 2.](../image/OrderItemMobile2.png "Order Item Classic Mobile 2")

4.  Tap **Edit** to edit your order, if required.

5.  To order the item as specified, tap **Order**, then tap **OK** when prompted to confirm ordering.

    A confirmation message appears.

    ![Screenshot for Classic Mobile order confirmation.](../image/OrderMobileConfirmation.png "Classic Mobile Order Confirmation")

6.  Tap the item to see further details.

    ![Screenshot for Classic Mobile Order Requested Item Details.](../image/OrderMobileRequestedItemDetails.png "Classic Mobile Order Requested Item Details")

7.  Tap the back arrow to return to the confirmation message.

8.  Tap **Continue Browsing** to return to the service catalog.

    After the request is submitted, ServiceNow follows request fulfillment processes to fulfill the ordered item.


-   **[Define the mobile layout](t_DefiningMobileLayout.md)**  
You can configure the Classic Mobile layout for categories within a service catalog.
-   **[Limit description sizes in the Classic Mobile UI](t_LimitDescriptionSizesInMobileUI.md)**  
By default, item descriptions in the smartphone interface are truncated to a maximum of two lines.

**Parent Topic:**[Service Catalog customization](../topic/p_ServiceCatalogCustomization.md)

