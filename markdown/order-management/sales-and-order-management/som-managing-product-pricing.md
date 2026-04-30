---
title: Configuring product pricing
description: Use the Pricing Management application to create the price lists and price list lines, define pricing adjustments, and manage other features that control pricing for product offerings. Product pricing is used by your sales and order agents when creating opportunities, quotes, and sales orders in Sales Customer Relationship Management.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-10-22"
reading_time_minutes: 6
breadcrumb: [Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configuring product pricing

Use the Pricing Management application to create the price lists and price list lines, define pricing adjustments, and manage other features that control pricing for product offerings. Product pricing is used by your sales and order agents when creating opportunities, quotes, and sales orders in Sales Customer Relationship Management.

## Pricing configuration overview

As a pricing administrator or pricing manager, you complete various configuration tasks and work with your product catalog administrator to set up the pricing for products and services sold by your organization. The following example workflow shows the pricing configuration tasks and how they fit within [product catalog and product offering configuration](som-managing-product-catalogs.md). You can also work with your administrator to extend certain pricing features, such as setting up pricing extension points to access pricing information from external sources.

![Workflow infographic that shows the main pricing configuration steps described in the following table, which also identifies other pricing features that can be configured](../image/q4-som-catalog-pricing-workflow.png "Product catalog and pricing configuration workflow")

Starting with the May 2024 release of Sales Customer Relationship Management applications, you can use the CSM Configurable Workspace to configure product pricing.

**Note:** Check your entitlements to determine if you have access to these features.

|Configuration task|Description|
|------------------|-----------|
|[Configurable pricing plans](configuring-pricing-plan.md)|Customize the default pricing plan provided with Pricing Management. You can add, change, or delete the sequence of steps in which pricing calculations and adjustments are run to determine product offering prices.|
|[Create and publish a price list](../task/som-create-price-list.md)|Define a price list that identifies basic pricing features, such as the currency used or the customer account to which the price list applies.|
|[Create a price list line](../task/som-create-price-list-line.md)|Add line items to a price list. A price list line identifies the list price for a product offering.|
|[Copy a price list](../task/copy-price-list.md)|Duplicate a published price list and its associated price list lines, attribute adjustments, and decision tables.|
|[Control the default price list on transaction header or header line](../task/som-control-default-pricelist.md)|Specify the conditions that control when a default price list is used for an opportunity, quote, or order by using the Price List Defaulting Matrix.|
|[Create and publish a product attribute-based pricing adjustment](../task/som-create-pricing-adjustment.md)|Define pricing adjustments based on certain product characteristics.|
|[Create and publish a cost book](../task/create-cost-books.md)|Create a cost book that identifies the currency of the unit costs defined for a set of product offerings.|
|[Create a cost book line](../task/create-cost-book-lines.md)|Add line items to a cost book. A cost book line defines the unit cost for a product offering. This feature is used in Quote Management, which uses unit costs to provide cost margins for products in sales quotes.|
|[Copy a cost book](../task/copy-cost-book.md)|Duplicate a cost book and its cost book lines.|
|[Control the default cost book on transaction header or header line](../task/som-control-default-costbook.md)|Set the default cost book displayed to your sales agents on the transaction header or header line for a Sales Customer Relationship Management application by using the Cost Book Defaulting Matrix.|
|[Create a non-product attribute pricing adjustment](../task/som-create-nonprod-attrib-adjustment.md)|Define pricing adjustments for products based on non-product characteristics such as shipping zip code, location, sales channel, or account segment by using the Standard Price Adjustment Matrix.|
|[Create pricing adjustments for bundled products](../task/som-create-bundle-adjustment.md)|Define the pricing adjustments for child product offerings in a bundled product by using the Configuration Component Price Adjustment Matrix.|
|[Create a matrix version](../task/create-matrix-versions.md)|Create a version of a published price matrix when you need to update the matrix, for example to add or delete a context variable used in the price matrix.|
|[Set properties to control pricing processing](../task/som-set-pricing-properties.md)|Manage the processing of pricing features, such as how certain pricing calculations are made.|
|[Create a custom context variable](../task/som-create-context-variable.md)|Create a custom variable that represents an attribute that can be used in a pricing matrix, for example to create a non-product attribute adjustment.|
|[Map a custom context variable to a transaction entity](../task/som-map-variable.md)|Associate a custom pricing context variable to a particular transaction entity type in Sales Customer Relationship Management.|
|[Use extension points in Pricing Management](extension-points-som-pricing.md)|Apply pricing extension points to use pricing information from external sources or extend the pricing engine logic on how list prices or adjustments are calculated.|
|[Export and import pricing entities](export-import-pricing-entities.md)|Export and import pricing entities between ServiceNow instances. For example, you can promote pricing entities such as price lists from a non-production instance to a production instance.|

