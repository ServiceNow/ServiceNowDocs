---
title: Product offer bundling with product specifications
description: Product Catalog Management supports the bundling of product offers that have associated product specifications or specification hierarchies at any level of the bundle.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Product offer bundling with product specifications

Product Catalog Management supports the bundling of product offers that have associated product specifications or specification hierarchies at any level of the bundle.

## Supported product offer bundles

As a product catalog admin or manager, you can create a bundle offer for the following product offer combinations:

-   A top-level offer with several offers in multiple levels, but no product specification reference at any level.
-   A top-level offer with several offers in multiple levels that can have a product specification reference at any level.
-   A top-level offer with two or three levels of nesting, where the leaf-level product offer references a specification hierarchy.

When offer bundles that have a specification reference at different levels are added to a quote or an order, the appropriate transaction lines are generated with specification references and product offer references. If fulfillment is done in ServiceNow Order Management, the applicable domain orders are generated and records for sold products and product inventory are created or updated.

## Characteristics inherited from product specifications

When you [create a product offering](som-create-product-offering.md) and reference a product specification hierarchy, you can select an option called **Copy child specification characteristics**. When you select this option, the product offer inherits all the characteristics from the specification or specification hierarchy. For example, if a product offer has an associated product specification, the characteristics are inherited from the child specifications in addition to the parent specification. The attributes from parent specification are always inherited by the product offer.

You can also do the following when you create a bundle product offering:

-   Add other characteristics to the offering, such as attributes for order enrichment, aside from characteristics inherited from the specification.
-   Delete product offering characteristics that were inherited from the specification.

To learn more about product offerings, see [Create product offerings](som-create-product-offering.md).

