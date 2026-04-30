---
title: Configure Service Catalog cart widgets
description: You can configure widgets for the shopping cart, catalog items, and order guides.You can customize the widget that provides details of the current catalog item on an order guide or wizard.You can customize widgets that appear for catalog items.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cart layout, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Catalog cart widgets

You can configure widgets for the shopping cart, catalog items, and order guides.

## Before you begin

Role required: admin

## About this task

Overview of configurable options in the Service Catalog on the Service Portal and explains how to perform those configurations.

**Parent Topic:**[Cart layout](../concept/c_ConfigureCartLayout.md)

## Configure order guide widgets

You can customize the widget that provides details of the current catalog item on an order guide or wizard.

### Before you begin

Role required: admin, catalog\_admin

### About this task

Order guide cart widget is visible when an order guide item is ordered.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**.

2.  Open the **Item Ordering Widget \(Order Guide\)** record.

3.  You can add/remove components and rename widget title.

4.  Click **Update**.

    ![](../image/OrderGuideWidget.png "Cart widget displayed for an order guide item")

    **Note:** By default, order guides use a two-step process, and catalog items use a one-step checkout process. If you configure the checkout process, keep in mind that order guides and catalog items provide different cart experiences if they use different checkout processes.


## Configure catalog item widgets

You can customize widgets that appear for catalog items.

### Before you begin

Role required: admin, catalog\_admin

### About this task

Both shopping cart and item ordering widgets are visible on the standard catalog page and any ESS catalog page. The shopping cart widget is also available in additional locations, such as the catalog homepage.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**.

    1.  Open the **Item Ordering Widget** record to modify the widget for ordering item.

    2.  Open the **Shopping Cart Widget** record to modify the widget for shopping cart.

2.  You can add/remove components, buttons, rename widget title and button labels.

3.  Click **Update**.

    ![](../image/CatalogItemWidgets.png "Item ordering and shopping cart widgets")


