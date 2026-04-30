---
title: Enable automatic updates to the wish list
description: Update the wish list automatically with user-specific changes from multiple tabs and platforms.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SC Wish List Cart widget, Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable automatic updates to the wish list

Update the wish list automatically with user-specific changes from multiple tabs and platforms.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home**.

    The Service Portal homepage is displayed.

2.  Access the wish list.

3.  Press and hold the Ctrl key, click the wish list widget, and select **Instance Options**.

4.  Select the **Auto update wish list** check box and click **Save**.

5.  Perform these additional steps only for upgrade customers.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.

    2.  In the banner, select **Portals**.

    3.  In the list, ensure that **Service Portal** is selected.

    4.  In the portal hierarchy chart, select **SP Header Menu**.

    5.  In the **Additional options, JSON format** field, set the `auto_update_wishlist` value as **true**.

        ```
        "auto_update_wishlist": {
                "displayValue": "true",
                  "value": true}
        ```

    ![Screenshot to automatically update the wish list](../image/auto-update-wish-list.png "Automatic updates to the wish list")


**Parent Topic:**[SC Wish List Cart widget](../concept/sc-wish-list.md)

**Related topics**  


[Enable the SC Wish List Cart widget in Service Portal](enable-wish-list-portal.md)

