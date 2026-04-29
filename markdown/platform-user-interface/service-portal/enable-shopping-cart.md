---
title: Enable the Shopping Cart widget
description: The shopping cart widget is enabled automatically for instances upgrading to Istanbul, however, there are several ways to manually enable or disable the widget.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SC Shopping Cart widget, Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable the Shopping Cart widget

The shopping cart widget is enabled automatically for instances upgrading to Istanbul, however, there are several ways to manually enable or disable the widget.

To enable the shopping cart for a catalog item:

1.  Navigate to a catalog item on the Service Catalog page in Service Portal.
2.  CTRL+right-click a catalog item widget to open the [widget instance options](c_ConfigureWidgetInstances.md).
3.  Select or clear the **Show Add Cart Button** option to enable or disable the shopping cart for that particular catalog item.

![Catalog item widget with the shopping cart item selected](../image/CatalogItemCartOption.png "Catalog item cart option")

To enable the shopping cart in the portal header:

1.  From the Service Portal configuration page, select the Portal editor.
2.  Select the SP Header Menu in the portal hierarchy.
3.  In the **Additional options** section, make sure the enable cart value is set to **true**.

    ```
    {
    	"enable_cart": {
    		"displayValue": "true",
    		"value": true
    	}
    }
    ```

    Set the value to **false** to hide the shopping cart.


![Header menu with shopping cart value set to true in the additional options section](../image/HeaderMenuShoppingCart.png "Shopping cart in the header menu")

**Parent Topic:**[SC Shopping Cart widget](sc-shopping-cart.md)

**Related topics**  


[Enable automatic updates to the shopping cart](../task/enable-auto-update-cart.md)

