---
title: Configuring product pricing
description: Use the Pricing Management application to create the price lists and price list lines, define pricing adjustments, and manage other features that control pricing for product offerings. Product pricing is used by your sales and order agents when creating opportunities, quotes, and sales orders in Sales Customer Relationship Management and by customers using self service for orders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/sales-and-order-management/som-managing-product-pricing.html
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuring product pricing

Use the Pricing Management application to create the price lists and price list lines, define pricing adjustments, and manage other features that control pricing for product offerings. Product pricing is used by your sales and order agents when creating opportunities, quotes, and sales orders in Sales Customer Relationship Management and by customers using self service for orders.

## Pricing configuration overview

As a pricing administrator or pricing manager, you complete various configuration tasks and work with your product catalog administrator and product catalog manager to set up the pricing for products and services sold by your organization. The following example workflow shows the pricing configuration tasks and how they fit within [product catalog and product offering configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-managing-product-catalogs.md). You can also work with your administrator to extend certain pricing features, such as setting up pricing extension points to access pricing information from external sources.

\[Omitted image "q4-som-catalog-pricing-workflow.svg"\] Alt text: Workflow infographic that shows the main pricing configuration steps described in the following table, which also identifies other pricing features that can be configured

You can use the CSM Configurable Workspace to configure product pricing.

**Note:** Check your entitlements to determine if you have access to these features.

|Configuration task|Description|
|------------------|-----------|
|Install Pricing Management|Install the Pricing Management application \(sn\_csm\_pricing\) if you have the admin role.|
|[Configurable pricing plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/configuring-pricing-plan.md)|Customize the default pricing plan provided with Pricing Management. You can add, change, or delete the sequence of steps in which pricing calculations and adjustments are run to determine product offering prices.|
|[Create and publish a price list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-create-price-list.md)|Define a price list that identifies basic pricing features, such as the currency used or the customer account to which the price list applies.|
|[Create a price list line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-create-price-list-line.md)|Add line items to a price list. A price list line identifies the list price for a product offering.|
|[Copy a price list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/copy-price-list.md)|Duplicate a published price list and its associated price list lines, attribute adjustments, and decision tables.|
|[Control the default price list on transaction header or header line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-control-default-pricelist.md)|Specify the conditions that control when a default price list is used for an opportunity, quote, or order by using the Price List Defaulting Matrix.|
|[Create a product attribute-based pricing adjustment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-create-pricing-adjustment.md)|Define pricing adjustments based on certain product characteristics.|
|[Create and publish a cost book](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/create-cost-books.md)|Create a cost book that identifies the currency of the unit costs defined for a set of product offerings.|
|[Create a cost book line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/create-cost-book-lines.md)|Add line items to a cost book. A cost book line defines the unit cost for a product offering. This feature is used in Quote Management, which uses unit costs to provide cost margins for products in sales quotes.|
|[Copy a cost book](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/copy-cost-book.md)|Duplicate a cost book and its cost book lines.|
|[Control the default cost book on transaction header or header line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-control-default-costbook.md)|Set the default cost book displayed to your sales agents on the transaction header or header line for a Sales Customer Relationship Management application by using the Cost Book Defaulting Matrix.|
|[Create a non-product attribute pricing adjustment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-create-nonprod-attrib-adjustment.md)|Define pricing adjustments for products based on non-product characteristics such as shipping zip code, location, sales channel, or account segment by using the Standard Price Adjustment Matrix.|
|[Create and publish a cost-based attribute adjustment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/create-cost-attribute-adjustment.md)|Define cost-based attribute adjustments for a cost book line or product offering.|
|[Create pricing adjustments for bundled products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-create-bundle-adjustment.md)|Define the pricing adjustments for child product offerings in a bundled product by using the Configuration Component Price Adjustment Matrix.|
|[Create a matrix version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/create-matrix-versions.md)|Create a version of a published price matrix when you need to update the matrix, for example to add or delete a context variable used in the price matrix.|
|[Set properties to control pricing processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-set-pricing-properties.md)|Manage the processing of pricing features, such as how certain pricing calculations are made.|
|[Enable ramps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-create-product-offering.md)|When creating a product offering, select the **Enable ramps** option, which lets sales agents add price and quantity ramps for the offering during the quote process. For information on how ramps work, see [Price and quantity ramps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/defining-products-with-ramps.md).|
|[Create a custom context variable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-create-context-variable.md)|Create a custom variable that represents an attribute that can be used in a pricing matrix, for example to create a non-product attribute adjustment.|
|[Map a custom context variable to a transaction entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/som-map-variable.md)|Associate a custom pricing context variable to a particular transaction entity type in Sales Customer Relationship Management.|
|[Use extension points in Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/extension-points-som-pricing.md)|Apply pricing extension points to use pricing information from external sources or extend the pricing engine logic on how list prices or adjustments are calculated.|
|[Export and import pricing entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/export-import-pricing-entities.md)|Export and import pricing entities between ServiceNow instances. For example, you can promote pricing entities such as price lists from a non-production instance to a production instance.|

