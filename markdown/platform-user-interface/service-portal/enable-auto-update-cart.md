---
title: Enable automatic updates to the shopping cart
description: Automatically update the shopping cart across all sessions when users make changes from multiple tabs and platforms.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SC Shopping Cart widget, Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable automatic updates to the shopping cart

Automatically update the shopping cart across all sessions when users make changes from multiple tabs and platforms.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home**.

    The Service Portal homepage is displayed.

2.  In the banner, click **Cart**.

3.  Press and hold the Ctrl key, click the wish list widget, and select **Instance Options**.

4.  Select the **Auto update cart** check box and click **Save**.

5.  Perform these steps only for upgrade customers.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.

    2.  In the banner, click **Portals**.

    3.  In the list, ensure that **Service Portal** is selected.

    4.  In the portal hierarchy chart, select **SP Header Menu**.

    5.  In the **Additional options, JSON format** field, set the `auto_update_cart` value as **true**.

        ```
        "auto_update_cart": {
                "displayValue": "true",
                  "value": true}
        ```

    ![Screenshot to automatically update the shopping cart](../image/auto-update-cart.png "Automatic updates to the shopping cart")


**Parent Topic:**[SC Shopping Cart widget](../concept/sc-shopping-cart.md)

**Related topics**  


[Enable the Shopping Cart widget](../concept/enable-shopping-cart.md)

