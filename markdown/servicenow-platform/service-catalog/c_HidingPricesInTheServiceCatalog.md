---
title: Hiding prices in the service catalog
description: Administrators can configure options to hide catalog item prices in the service catalog for listings of specific items, for specific types of items, or for all items.Configure service catalog properties to hide prices globally.You can hide prices for specific items to match your organizational requirements.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hiding prices in the service catalog

Administrators can configure options to hide catalog item prices in the service catalog for listings of specific items, for specific types of items, or for all items.

Item prices can appear in the following locations:

-   A catalog item listing in the **Order This Item** panel.
-   Catalog item listings in categories and subcategories.
-   The **Shopping Cart** panel.
-   The Edit Cart, Order Confirmation, and Order Status pages.

**Parent Topic:**[Service Catalog customization](../topic/p_ServiceCatalogCustomization.md)

## Hide prices globally

Configure service catalog properties to hide prices globally.

To view and edit service catalog properties, navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

### Hiding prices by item types

By default, prices do not appear for order guides, record producers, and wizard launchers.

You can change which catalog item types show prices using the **List of class names for catalog items that do not show the price in listings** property \(**glide.sc.item.cannot\_show\_price**\). Provide a comma-separated list of table names for item types that you want to hide prices for.

For example, to hide prices for standard catalog items, add **sc\_cat\_item** to the list.

You can also remove an existing entry to display prices for that item type. For example, to display prices for order guides, remove the order guide entry **sc\_cat\_item\_guide** from the list.

### Hiding prices for all items

By default, zero-priced items have prices hidden in listings and carts.

You can configure this behavior to always hide or show prices, using the **When to show prices and sub-totals on the Service Catalog Cart** property \(**glide.sc.price.display**\).

Set this property to **Always show prices** to display prices for all items on all service catalog screens, or to **Never show prices** to hide prices for all items on all service catalog screens.

## Hide prices for specific items

You can hide prices for specific items to match your organizational requirements.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

2.  Open the relevant item definition.

3.  Select the **Omit Price on Cart** check box.

    The price does not appear in the catalog listing or when the item is added to the cart. The price is listed as "-" on the edit cart, order confirmation, and order status screens.


