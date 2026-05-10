---
title: SC Shopping Cart widget
description: The SC Shopping Cart widget \(sc-shopping-cart-v2\), used with Service Catalog, stores all your orders at one place. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# SC Shopping Cart widget

The SC Shopping Cart widget \(sc-shopping-cart-v2\), used with Service Catalog, stores all your orders at one place. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

Use the shopping cart widget to:

-   Control the quantity of items in the cart.
-   Add items to a cart. This information is stored in the sc\_cart table.
-   Define who the items are being requested for.
-   Save specific items together as a bundle, which can be reloaded later. You can replace the cart items with the saved bundles, or add the bundles to the cart items.
-   Remove all items from your cart.

![Screenshot for the SC Shopping Cart widget](../../../product/service-catalog-management/image/SCShoppingCart.png "SC Shopping Cart widget")

## Instance options

Use the widget instance options to customize the settings for the SC Shopping Cart widget. To customize the settings for this widget, press the Ctrl key, click on the widget, and select **Instance Options**.

|Field|Description|
|-----|-----------|
|Presentation|
|Bootstrap color|Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.|
|Behavior|
|Cart Template|Enter the name of a ng-template you want to use to provide a different template for the shopping cart. By default, two ng-templates are provided: `small_shopping_cart_v2.html` and `large_shopping_cart_v2.html`.|
|Auto update cart|Automatically updates the cart across all sessions.|

-   **[Enable the Shopping Cart widget](enable-shopping-cart.md)**  
The shopping cart widget is enabled automatically for instances upgrading to Istanbul, however, there are several ways to manually enable or disable the widget.
-   **[Enable automatic updates to the shopping cart](../task/enable-auto-update-cart.md)**  
Automatically update the shopping cart across all sessions when users make changes from multiple tabs and platforms.

**Parent Topic:**[Service Catalog widgets](sc-widgets.md)

**Related topics**  


[Catalog Content widget](catalog-content-widget.md)

[Catalog Homepage Search widget](cat-homepage-search-widget.md)

[Recent &amp; Popular Items widget](recent-and-popular-items-widget.md)

[Request Fields widget](request-fields-widget.md)

[Requested Items widget](requested-items-widget.md)

[Requests and Approvals widget](requests-and-approvals-widget.md)

[SC Catalog Item widget](sc-catalog-item-widget.md)

[SC Categories widget](sc-categories-widget.md)

[SC Category Page widget](sc-category-page-widget.md)

[SC Order Guide widget](sc-order-guide-widget.md)

[SC Popular Items widget](sc-popular-items.md)

[SC Save Bundles widget](save-bundles-widget.md)

[SC Saved Carts widget](saved-cart-widget.md)

[SC Scroll to top widget](sc-scroll-to-top.md)

[SP Variable Editor widget](variable-editor-widget.md)

[SC Wish List Cart widget](sc-wish-list.md)

[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

[Add a catalog item to the shopping cart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/add-to-cart-portal.md)

