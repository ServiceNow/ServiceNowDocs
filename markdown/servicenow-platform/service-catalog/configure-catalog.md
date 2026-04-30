---
title: Configure catalogs
description: Enable your users to view and request their associated items in the Now Mobile app. If no catalogs are selected, users can view and request items from all catalogs in the system. By default, the app uses Service Catalog.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request experience in Now Mobile, Service Catalog in mobile, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure catalogs

Enable your users to view and request their associated items in the Now Mobile app. If no catalogs are selected, users can view and request items from all catalogs in the system. By default, the app uses Service Catalog.

## Before you begin

Role required: admin

## About this task

Demonstrates configuring service catalogs, knowledge bases, and My Requests in the Now Mobile App.

## Procedure

1.  Navigate to **All** &gt; **Now Mobile App** &gt; **Catalogs**.

2.  In the portal catalogs \[m2m\_sp\_portal\_catalog\] table, add a catalog in addition to the base system catalog, or change the catalog that is associated with the base system record:

    1.  Click **New** or open the base system record.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Portal|Portal that you select. Select **Employee Center**.|
        |Catalog|Catalog that you would like to associate with the app.|
        |Order|Number that indicates the order that the configurations should run. If there are multiple configurations on a portal, the system runs the configurations from the lowest to the highest order that you selected.|


## Result

Your users can view and request items from all added catalogs.

**Parent Topic:**[Request experience in Now Mobile](../../../product/service-catalog-management/concept/now-mobile-catalog.md)

**Related topics**  


[Browse catalog items using the catalog hierarchy](../../../product/service-catalog-management/task/now-mob-browse-cat-item-catalog.md)

[Submit and track a request](order-item.md)

[Create a quick action in your mobile applications](sc-quick-action.md)

[Enable notifications in Now Mobile](../../../product/service-catalog-management/task/enable-notification-mobile.md)

[Enable the cart in Now Mobile](../../../product/service-catalog-management/task/enable-cart-mobile.md)

[Edit the label of Submit button for a record producer](../../../product/service-catalog-management/task/edit-recprdcr-submit-label.md)

[Configure Now Mobile properties](../../../product/service-catalog-management/task/config-now-mob-properties.md)

