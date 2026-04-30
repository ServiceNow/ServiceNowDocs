---
title: Remove item restrictions
description: Service Catalog enables you to remove or apply restrictions on all order guides, record producers, and wizard launchers.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Remove item restrictions

Service Catalog enables you to remove or apply restrictions on all order guides, record producers, and wizard launchers.

## Before you begin

Role required: admin

## About this task

Catalog administrators can use Service Catalog properties to configure the behavior and usage of a catalog item.

By default, all order guides, record producers, and wizard launchers have these restrictions:

-   They cannot be added to a requested item
-   They do not provide a **Try It** action
-   They are not added to the cart as items

To remove these restrictions or apply these restrictions to other types of items:

## Procedure

1.  Modify the comma-separated lists of tables in the following properties:

    -   **List of class names for catalog items that cannot be added to an existing request**\(**glide.sc.item.cannot\_add\_to\_request**\): restricts the items that can be added to a requested item, after an end user places a request. For example, to restrict content items from being added to an existing request, add sc\_cat\_item\_content to the list for this property.
    -   **List of class names for catalog items that do not use the default "Try It" UI Action**\(**glide.sc.item.cannot\_try\_it**\): restricts the items which allow you to click **Try It** on the item form to preview how it appears in the service catalog. Items with such restrictions do not display **Try It** on the form.
    -   **List of class names for catalog items that do not generate a normal cart item**\(**glide.sc.item.not\_normal\_cart\_item**\): restricts which item types are added to the cart by default.

**Parent Topic:**[Service Catalog customization](../topic/p_ServiceCatalogCustomization.md)

