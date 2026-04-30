---
title: Add a supplier product bundle
description: Add a supplier product bundle, which may include several products or services from the same supplier. You can also add sub-bundles to the main bundle.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up your product catalog, Setting up primary data for ShoppingHub, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add a supplier product bundle

Add a supplier product bundle, which may include several products or services from the same supplier. You can also add sub-bundles to the main bundle.

## Before you begin

A bundled model is a single model comprised of individual models. For example, a laptop, printer, keyboard, and mouse can be combined into a single bundled model. For this bundled model to appear in the Shopping Hub portal, you have to create a supplier product for the same. Once the supplier product is created and published, it will be available for purchase in Shopping Hub. For more information on how to create bundled models, see [Bundled models](https://www.servicenow.com/docs/bundle/washingtondc-it-asset-management/page/product/product-catalog/concept/c_CreatingBundledModels.html).

Role required: sn\_shop.shopping\_hub\_admin or sn\_shop.procurement\_administrator

## About this task

A supplier product bundle is a supplier product created under any product model of type bundle.

You can add a supplier product bundle and choose to publish it on the Shopping Hub portal. The product bundles that you add appear on the portal under various categories. To a product bundle you can add multiple products, services, or sub-bundles that are available with the same supplier.

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Supplier Products** &gt; **Published Products**.

    You can also navigate to **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Supplier Product**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information, see [Add a supplier product](add-supplier-product.md).

    **Note:** For creating a product bundle, enter the product model of type bundle in the **Product model** field.

4.  Select **Check bundle setup** to check if the configurations for all the products and services included in the bundle are complete.

    For all missing configurations, a list of validation messages are displayed. You can select each message to correct the respective configuration. The following conditions must be fulfilled for publishing a bundle:

    -   All model components must be associated with supplier products from the same supplier.
    -   All supplier products must be published.
    -   All supplier products other than type bundle must have a contract price associated with them.
    -   All supplier products of type bundle must not have a contract price associated with them.
    -   All supplier products must have a contract price listed in the same currency.
    **Note:** If **Check bundle setup** option is selected for an already published bundle and any of its configurations are found incomplete, the bundle gets unpublished.

5.  Select **Submit**.


## What to do next

Use the related lists of the supplier product form to view the pricing, purchase order lines, product visuals, and ledger assignment rules that are associated with this supplier product bundle.

**Parent Topic:**[Setting up your product catalog](create-product-catalogue.md)

