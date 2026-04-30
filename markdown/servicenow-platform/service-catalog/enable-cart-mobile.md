---
title: Enable the cart in Now Mobile
description: Allow a requester to add or edit items in the cart. By default, the cart is disabled in Now Mobile.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request experience in Now Mobile, Service Catalog in mobile, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable the cart in Now Mobile

Allow a requester to add or edit items in the cart. By default, the cart is disabled in Now Mobile.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to sys\_properties.list.

2.  For the **glide.sc.cart.enabled** property, specify **Value** as `true`.

3.  Click **Update**.

    The Cart icon is displayed at the top of the app and the **Add to Cart** button is enabled for items.


**Parent Topic:**[Request experience in Now Mobile](../concept/now-mobile-catalog.md)

**Related topics**  


[Configure catalogs](../../../administer/mobile-employee/task/configure-catalog.md)

[Browse catalog items using the catalog hierarchy](now-mob-browse-cat-item-catalog.md)

[Submit and track a request](../../../administer/mobile-employee/task/order-item.md)

[Create a quick action in your mobile applications](../../../administer/mobile-employee/task/sc-quick-action.md)

[Enable notifications in Now Mobile](enable-notification-mobile.md)

[Edit the label of Submit button for a record producer](edit-recprdcr-submit-label.md)

[Configure Now Mobile properties](config-now-mob-properties.md)

