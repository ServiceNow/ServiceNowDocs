---
title: Add a Shopping Hub icon link to your service portal
description: You can add a Shopping Hub icon link to your service portal icons menu so that shoppers can navigate from the service portal to the Shopping Hub portal with a single select.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service portal configuration for ShoppingHub, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add a Shopping Hub icon link to your service portal

You can add a Shopping Hub icon link to your service portal icons menu so that shoppers can navigate from the service portal to the Shopping Hub portal with a single select.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration** &gt; **Designer**.

2.  From the Service Portal Designer, select the Service Portal home page.

3.  From **Layouts**, select **Container** and drag it onto the page.

    **Note:** You must add a 4-column container here.

4.  From **Widgets**, drag **Icon Link** and drop it in the container.

5.  On the **Icon Link** container, select the **Edit** icon.

6.  On the Instance with Link form, fill in these fields:

    1.  On the **Type** field, select **URL**.
    2.  In the **HREF / URL** field, enter **/now/shopnow?ref=sp\_icon**.
    3.  In the **Title** field, enter **Buy something**.
    4.  In the **Short description** field, enter **Visit our procurement portal to purchase goods or services from any supplier**.
    5.  On the **Glyph** field, select the **Basket** icon.
    6.  On the **Template** field, select **Circle icon**.
    **Note:** It is recommended that you use these settings. However, you can configure this otherwise as well.

7.  Select **Save**.


**Parent Topic:**[Service portal configuration for ShoppingHub](../concept/service-portal-configuration-for-shoppinghub.md)

