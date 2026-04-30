---
title: Migrate customizations and enable cart layouts
description: Move customization to cart layout widgets, and then enable cart layouts.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Migrating to cart layouts, Cart layout, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Migrate customizations and enable cart layouts

Move customization to cart layout widgets, and then enable cart layouts.

## Before you begin

Role required: admin

## About this task

When you customize a few UI macros, you should migrate the customizations to cart layout widgets before you enable cart layouts.

Following are the UI macros whose customizations need migration before you enable cart layouts:

-   sc\_catalog\_homepage\_cart
-   sc\_catalog\_requested\_for
-   catalog\_item
-   catalog\_cart\_default
-   sc\_cart\_main

In addition, if you have customized the com.glideapp.servicecatalog\_category\_view UI page, or the Catalog Cart dynamic content, you must migrate these customizations before you enable cart layouts.

## Procedure

1.  Save copies of the customizations for later reference.

2.  Revert the customizations to restore the customized macros or other content to their standard state.

3.  Remove the record for the customization from the Customer Update \[sys\_update\_xml\] table.

4.  Run the following script in Background Scripts to set the property and set the correct state for all the items in the catalog:

    ```
    var cm = new CartLayoutMigration();cm.configureLayoutProperty();cm.setLayoutFalse();cm.setEmptyLayout();
    ```

5.  Reimplement any cart layout customizations that you want to maintain in the upgraded instance by configuring widget macros.

6.  To enable cart layouts, set the service catalog system property **glide.sc.use\_cart\_layouts** to **Yes**.


**Parent Topic:**[Migrating to cart layouts](../concept/c_MigrateCartLayouts.md)

