---
title: SC Shopping Cart widget
description: The SC Shopping Cart widget \(sc-shopping-cart-v2\), used with Service Catalog, stores all your orders at one place. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/sc-shopping-cart.html
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

\[Omitted image "SCShoppingCart.png"\] Alt text: Screenshot for the SC Shopping Cart widget

## Instance options

Use the widget instance options to customize the settings for the SC Shopping Cart widget. To customize the settings for this widget, press the Ctrl key, click on the widget, and select **Instance Options**.

|Field|Description|
|-----|-----------|
|Presentation|
|Bootstrap color|Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.|
|Behavior|
|Cart Template|Enter the name of a ng-template you want to use to provide a different template for the shopping cart. By default, two ng-templates are provided: `small_shopping_cart_v2.html` and `large_shopping_cart_v2.html`.|
|Auto update cart|Automatically updates the cart across all sessions.|

-   **[Enable the Shopping Cart widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/enable-shopping-cart.md)**  
The shopping cart widget is enabled automatically for instances upgrading to Istanbul, however, there are several ways to manually enable or disable the widget.
-   **[Enable automatic updates to the shopping cart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/enable-auto-update-cart.md)**  
Automatically update the shopping cart across all sessions when users make changes from multiple tabs and platforms.

**Parent Topic:**[Service Catalog widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/sc-widgets.md)

**Related topics**  


[Catalog Content widget]()

[Catalog Homepage Search widget]()

[Recent &amp; Popular Items widget]()

[Request Fields widget]()

[Requested Items widget]()

[Requests and Approvals widget]()

[SC Catalog Item widget]()

[SC Categories widget]()

[SC Category Page widget]()

[SC Order Guide widget]()

[SC Popular Items widget]()

[SC Save Bundles widget]()

[SC Saved Carts widget]()

[SC Scroll to top widget]()

[SP Variable Editor widget]()

[SC Wish List Cart widget]()

[Create and edit a page using the Service Portal Designer]()

[Configure widget instances]()

[Clone a widget]()

[Add a catalog item to the shopping cart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/add-to-cart-portal.md)

