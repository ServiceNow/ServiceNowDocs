---
title: Enable the SC Wish List Cart widget in Service Portal
description: Add catalog items or record producers to the wish list after you enable the wish list.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SC Wish List Cart widget, Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable the SC Wish List Cart widget in Service Portal

Add catalog items or record producers to the wish list after you enable the wish list.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Maintain Catalogs**.

2.  From the Catalogs list, select **Service Catalog**.

3.  On the catalog form, select the **Enable Wish List** check box and click **Update**.

    The **Wish List** menu option is displayed in the Service Portal banner.

    **Note:** The **Use the sc\_layout driven cart macros \(default true\)** \(**glide.sc.use\_cart\_layouts**\) property must be set to true to enable the wish list.

4.  To enable the **Wish List** menu option in the Service Portal banner, perform these additional steps only for upgrade customers.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.

    2.  In the banner, click **Portals**.

    3.  In the list, ensure that **Service Portal** is selected.

    4.  In the portal hierarchy chart, select **SP Header Menu**.

    5.  In the **Additional options, JSON format** field, set the `enable_wishlist` value as **true**.

        ```
        "enable_wishlist": {
                "displayValue": "true",
                  "value": true}
        ```

    ![Screenshot to enable the SC Wish List Cart widget](../image/EnableWshList.png "Enable the SC Wish List Cart widget")

5.  Enable the Add to Wish List icon \(![](../image/SPWishList.png)\) in the Ordering widget of a catalog item or record producer:

    1.  Navigate to **Service Portal** &gt; **Service Portal Home** &gt; **Order Something**.

        The Service Portal homepage is displayed.

    2.  Click one of the available catalog items.

    3.  Press and hold the Ctrl key, click a catalog item widget, and select **Instance Options**.

    4.  Select the **Show Add/Update Wish List buttons** check box and click **Save**.


**Parent Topic:**[SC Wish List Cart widget](../concept/sc-wish-list.md)

**Related topics**  


[Enable automatic updates to the wish list](enable-auto-update-wish-list.md)

