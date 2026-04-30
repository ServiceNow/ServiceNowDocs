---
title: Quote Management
description: Quote Management is an application used to create and manage product quotes. Quote Management can be a separate application or part of the Sales Customer Relationship Management \(SOM\) application.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Quote Management

Quote Management is an application used to create and manage product quotes. Quote Management can be a separate application or part of the Sales Customer Relationship Management \(SOM\) application.

A quote is a formal offer for products and services, proposed at specific prices and related payment terms, which is sent to a prospective customer or consumer. In the context of Sales Customer Relationship Management, quotes can be created from the Opportunity Management application or quotes can be created separately, depending on your configuration.

![Sales and Order Management workflow that shows the opportunity, quote, and order creation steps.](../image/l2c-quote-workflow-5.png "Quote workflow in Sales Customer Relationship Management")

## Quote Management interface

The Quote Management application is integrated with the product offering catalog and product configurator to help sales agents build quotes easily and conveniently. The Quote Management interface contains the following tabs:

|Tab|Description|
|---|-----------|
|[Details tab](../task/quote-management-details-tab.md)|Add basic information for the quote.|
|[Catalog tab](../task/quote-management-catalog-tab.md)|Search for and add products to your quote using the product configurator. Pricing is also managed through the product offering catalogs.|
|[Line Items tab](../task/quote-managment-line-items-tab.md)|Add different line items to a quote. In each quote line item, you can update product characteristics and add pricing adjustments.|
|[Revisions tab](../task/quote-management-revisions-tab.md)|Create multiple versions of a quote.|
|[Customer Orders tab](../task/quote-management-customer-orders-tab.md)|Turn your quote into a customer order.|
|[Pricing Adjustment tab](../task/quote-management-pricing-adjustments-tab.md)|View and update pricing adjustments.|

![The Quote Management Details tab used to enter all the basic quote information. The image also shows additional tabs used to build the quote.](../image/l2c_quote-main-window.png "Quote Management Details tab")

## Quote Management integration with product offering catalogs

Quote Management is integrated with the product catalog and pricing to make adding products to your quote easier and convenient. Agents use the catalog to browse product offerings and the product configurator to add options and pricing to your products. Then they simply add them to the quote. Pricing adjustments that are fetched based on pricing matrices rules are automatically added and presented in the quote.

## Product configurator

The product configurator lets your agents configure products in the following ways:

-   Browse and add configurable product offerings from the catalog to create quote lines.
-   Select product options and view product relationships.

The product configurator uses Sales Customer Relationship Management primitives to create and update quote lines and characteristics.

![Shows the product configurator that lets agents select options for products before they add the product to the quote.](../image/l2c-quote-product-customize.png "Building a quote with the product configurator")

## Configure and create quote line items

From the product catalog, browse and add product offers to create quote lines and characteristics.

With the product configurator, characteristics options and relationships can be changed and updated in the Catalog tab for Quote Management. The product configurator uses Quote Management primitives to create and update quote lines and characteristics.

## Add pricing adjustments to quotes

Quote Management integrates with the pricing engine to get the list price and price adjustments for the product offers in your quote.

Auto-pricing adjustments are fetched from the pricing engine. Manual pricing adjustments are added by the agent.

Pricing adjustments include markups, markdowns, and price overrides. Total Adjustments are applied to each line item with the cumulative total from each line rolled up to total.

Quote Management lets sales agents add the following types of manual pricing adjustments:

-   Markup amount - add a markup amount to a product.
-   Markdown amount - add a markdown amount to a product.
-   Markup % - add a markup percentage to a product.
-   Markdown % - add a markdown percentage to a product.
-   Price override - override a price and set a new price.

## Adding cost books in Quote Management

A cost book contains the unit costs for product offerings. Cost books provide your agents with the following benefits:

-   Profit margin calculation: Ability to calculate the profit margin by subtracting the cost price from the quoted selling price, helping your sales team verify that their pricing strategy aligns with desired profit margins,
-   Discount management: Apply discounts to quotes based on cost prices to incentivize bulk purchases or long-term commitments for flexible pricing strategies while maintaining profitability and competitive incentives to your customers.​
-   Negotiation support: Use cost prices as a reference during negotiations with your customers or suppliers. It provides a transparent basis for discussions, helping you build trust and facilitating fair and mutually beneficial agreements.​

To learn more about cost books and their configuration, see [Pricing Management](pricing-management.md), [Create and publish a cost book](../task/create-cost-books.md), [Create a cost book line](../task/create-cost-book-lines.md), and [Install and configure Quote Management](configure-quote-management.md).

## Creating PDF documents in Quote Management

Once your quote is completed, you can send it to customers for review and signing by creating a pdf and emailing it. The pdf can be configured with logos and also connected to services like Docusign. This allows you to communication and confirm quote offerings.

## View line items as a hierarchical list

Sales Agent view quote line items as a hierarchical list, which helps organize quote with many line items.

## What to do next

To learn about setting up Quote Management, see [Install and configure Quote Management](configure-quote-management.md).

