---
title: Publish a data product
description: Publish a data product to make it available to consumers in the Data Catalog.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Managing data products, Data Products, Workflow Data Fabric]
---

# Publish a data product

Publish a data product to make it available to consumers in the Data Catalog.

## Before you begin

Role required: data\_product\_admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Data Workbench**.

2.  In Data Workbench, open the data product and select **Publish**.

    The **Publish** button is available only when the data product is in draft state.

    ![Publish a data product](../image/wdf-data-product-publish.png)

3.  Review the confirmation and select **Publish**.

    The data product state updates to **Published**.

4.  To make changes to a published data product, select **Edit** on the details page.

    This returns the data product to draft state. You can republish it when your changes are complete.


## Result

The data product is published. After the metadata collector runs, it appears in the Data Catalog. Consumers can discover and request access to it.

**Important:** A delay occurs between publishing a data product and its appearance in the Data Catalog. The metadata collector must run before the data product is discoverable. To make it available without waiting for the scheduled run, ask your administrator to run the collector manually from Connect Hub.

## What to do next

To move the data product to production instance, see [Move data interfaces and data products to production](move-data-interfaces-products-to-prod-wdf.md)

**Parent Topic:**[Managing data products](../concept/manage-data-products-wdf.md)

