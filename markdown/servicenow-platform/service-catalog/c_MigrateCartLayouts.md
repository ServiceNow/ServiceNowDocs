---
title: Migrating to cart layouts
description: Service catalog enables you to configure cart layouts to add, remove, or change elements of the service catalog shopping cart. Before you migrate your system to use cart layouts, familiarize yourself with existing configurations for catalog content and decide whether to discard or retain these configurations.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cart layout, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Migrating to cart layouts

Service catalog enables you to configure cart layouts to add, remove, or change elements of the service catalog shopping cart. Before you migrate your system to use cart layouts, familiarize yourself with existing configurations for catalog content and decide whether to discard or retain these configurations.

This feature is enabled by default in new instances and the default cart layout settings are implemented. For upgrades, an upgrade script checks to see if your current cart macros are customized. Only a user with an admin role can migrate cart layouts.

-   If cart macros are not customized, cart layout configuration is enabled by default.
-   If cart macros are customized, cart layout configuration is disabled. Migrate your system to use this feature.

## Cart configuration settings

Check your current configurations for:

-   UI macros defining custom shopping carts that have been linked to items.
-   Service catalog properties impacted by cart layouts.
-   Item-specific settings that can override cart layout record settings.

## Item-specific settings

Some catalog items can have cart layout settings that are specific to them.

For example, these items can show prices even though the general cart layout record settings hide prices.

To retain item-specific settings, clear the **Use cart layout** check box in the catalog item form.

![Screenshot for item-specific settings](../image/Service_Catalog_Use_Cart_Layout.png "Item-specific settings")

**Note:** You can configure the form to display the **Use cart layout** check box.

-   **[Migrate customizations and enable cart layouts](../task/t_MoveCustomizationsToCartLayouts.md)**  
Move customization to cart layout widgets, and then enable cart layouts.

**Parent Topic:**[Cart layout](c_ConfigureCartLayout.md)

