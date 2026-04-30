---
title: Configuring product offerings and catalogs
description: Create product offerings and the associated product catalogs that can be used by Sales Customer Relationship Management agents for pre-sales activities, order capture, and post-sales engagement.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configuring product offerings and catalogs

Create product offerings and the associated product catalogs that can be used by Sales Customer Relationship Management agents for pre-sales activities, order capture, and post-sales engagement.

As a product catalog administrator or catalog manager, you complete various configuration tasks to create the product catalogs and offerings for products and services sold by your organization. You also work with your pricing administrator, who sets the pricing for your product offerings. For more information on pricing, see [Configuring product pricing](som-managing-product-pricing.md).

The following workflow example shows a typical series of steps for setting up catalogs and product offerings, including the pricing configuration tasks performed by your pricing administrator. Some steps may be optional in your organization, and other steps, such as setting up product relationships between catalog entities, may occur in a slightly different sequence.

![Workflow infographic that shows the main product catalog configuration steps, which are described in the following table along with other product catalog features that can be configured.](../image/q4-som-catalog-pricing-workflow.png "Product catalog and pricing configuration workflow")

**Note:** Review your entitlements to see the product offering options available to you.

## Overview of product offering and catalog configuration

Starting with the May 2024 release of Sales Customer Relationship Management applications, you can use the CSM Configurable Workspace to configure product offering catalogs, product offerings, and product offering relationships.

The following table identifies the configuration tasks for setting up the various features available in Product Catalog Management.

|Configuration task|Description|
|------------------|-----------|
|[Create a product offering catalog](../task/som-create-product-catalog.md)|Create a catalog, which is the top-level entity in the catalog hierarchy. Catalogs can have categories, and categories can have subcategories or product offers.|
|[Create a product offering category](../task/som-create-product-offering-category.md)|Define a product offering category used to organize similar product offerings in a catalog. Catalog categories make it easier for agents to browse and navigate product offerings when creating opportunities, quotes, and orders.|
|[Create product characteristics and characteristic options](../task/som-product-config-add-characteristics.md)|Define the specific attributes, properties, and options that distinguish a product offering, influencing its configuration and pricing.|
|[Create product offerings](../task/som-create-product-offering.md)|Configure and add product offerings to catalogs and categories. Once published, product offerings are available to Sales Customer Relationship Management agents as they create opportunities, quotes, and orders.|
|[Add product visuals](../task/som-product-config-add-visuals.md)|Add images and thumbnails to your product offerings to help agents as they build opportunities, quotes, and orders.|
|[Create product offering relationships](../task/som-product-config-offering-relationships.md)|Create product relationships to bundle products and services together to streamline the order process. Product offering relationships drive the order capture experience by letting you group multiple product offerings into bundles. Bundles also let you offer special bundle pricing.|
|[Control cascading quantity values in child product offerings](../task/som-activate-cascade-quantity.md)|Control how the quantities for child line items in a product offering for a quote or order are calculated by using the **sn\_prd\_pm.enable\_cascade\_quantity** system property.|
|[Add related contracts to product offerings](../task/som-product-config-related-contracts.md)|Add related contracts to your product offerings in the Sales Customer Relationship Management application.|
|[Add a unit of measure to a product offering](../task/som-product-config-add-unit-of-measure.md)|Add a unit of measure \(UOM\) to a product offering in Sales Customer Relationship Management.|
|[Create a product offering version](../task/som-product-config-create-new-version.md)|Create a product version to add updates to a published product offering.|
|[Create product offering relationship groups](../task/som-product-config-relationship-groups.md)|Combine bundles of product offerings into related groups in Sales Customer Relationship Management.|
|[Configure needs analysis](configuring-needs-analysis.md)|Create needs templates, which are questionnaires from product selection guides that your agents use to determine what product offers can be added to opportunities.|
|[Export and import product catalog entities](export-import-product-catalog-entities.md)|Export and import product catalog entities between ServiceNow instances. For example, you can promote catalog entities from a non-production instance to a production instance.|
|[View product offering hierarchy and associated specification hierarchy](som-catalog-hierarchy.md)|View the complete hierarchy of a product offering and any associated specifications \(product, service, and resource\). Use these views to verify that all entities have been defined and associated correctly.|
|[Configure product offer eligibility](configuring-sales-eligibility.md)|Filter the product catalog, product categories, and product offerings dynamically, to display only eligible product offerings for a customer in the product catalog.|

