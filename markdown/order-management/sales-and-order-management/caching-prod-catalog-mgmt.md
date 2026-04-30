---
title: Caching in Product Catalog Management
description: The Product Catalog Management application uses caching to improve user interface performance when agents access product catalogs and product offerings through the product configurator.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Caching in Product Catalog Management

The Product Catalog Management application uses caching to improve user interface performance when agents access product catalogs and product offerings through the product configurator.

## Overview

The product offering catalog and configurable product offerings have hierarchical structures that require frequent database retrieval when they’re used. To improve performance, these hierarchical structures are cached when you publish these features.

As a product catalog admin or manager, when you make the following changes to a published product offering or product offering catalog, you must update the associated cache so that you can immediately see the changes just made:

-   **Unit of Measure** \(UOM\) in product offerings – Although product offerings cannot be changed after you publish them, you can change the default **Unit of Measure**. After updating the UOM, you must update the product offering cache.
-   **Product offering catalog changes** – If you change the hierarchies for catalog to category or category to sub-category hierarchies, you must update the product offering catalog cache.

For details on regenerating these caches, see [Update a cache in Product Catalog Management](../task/som-update-cache-catalog-mgmt.md).

