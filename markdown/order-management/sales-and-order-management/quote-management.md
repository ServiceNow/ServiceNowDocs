---
title: Quote Management
description: Quote Management is an application used to create and manage product and service quotes. Quote Management can be a separate application or part of the Sales Customer Relationship Management \(SOM\) application.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Quote Management

Quote Management is an application used to create and manage product and service quotes. Quote Management can be a separate application or part of the Sales Customer Relationship Management \(SOM\) application.

A quote is a formal offer for products and services, proposed at specific prices and related payment terms, which is sent to a prospective customer or consumer. In the context of Sales Customer Relationship Management, quotes can be created from the Opportunity Management application or quotes can be created separately, depending on your configuration.

![Image shows the quote workflow for a sales agent.](../image/quote-workflow-1.png "Quote workflow in Sales Customer Relationship Management")

## Quote Management user interface

The Quote Management application is integrated with the product offering catalog and product configurator to help sales agents build quotes easily and conveniently. The Quote Management interface contains the following tabs:

<table id="table_vsl_wh2_fbc"><thead><tr><th>

Quote window tabs or options

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Details tab](../task/quote-management-details-tab.md)

</td><td>

Add basic information for the quote.

</td></tr><tr><td>

[Catalog tab](../task/quote-management-catalog-tab.md)

</td><td>

Search for and add products to your quote using the product configurator. Pricing is also managed through the product offering catalogs.

</td></tr><tr><td>

[Line Items tab](../task/quote-management-line-items-tab.md)

</td><td>

Add different line items to a quote. In each quote line item, you can update product characteristics and add pricing adjustments.

</td></tr><tr><td>

[Revisions tab](../task/quote-management-revisions-tab.md)

</td><td>

Create multiple versions of a quote.

</td></tr><tr><td>

[Customer Orders tab](../task/quote-management-customer-orders-tab.md)

</td><td>

Turn your quote into a customer order.

</td></tr><tr><td>

[Pricing Adjustment tab](../task/quote-management-pricing-adjustments-tab.md)

</td><td>

View and update pricing adjustments.

</td></tr><tr><td>

[Enable a sales agreement in a quote](../task/quote-create-sales-agreement.md)

</td><td>

When the sales agreement is enabled, the quote workflow changes and enables agents to add products and services according to the sales agreement.

</td></tr><tr><td>

[Create a quote PDF document](../task/quote-create-pdf-document.md)

</td><td>

Sales agents can create a PDF document from a quote to send to customers for review and signatures.

</td></tr><tr><td>

**Channel Partner [Quote management for business organization](https://www.servicenow.com/docs/access?context=quote-management-for-business-location&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

</td><td>

Channel partners with multiple locations can create and manage the quote related parties in case of multi-partners sales. They can also view detailed price breakdowns on quote line items.

</td></tr><tr><td>

**Quote Related Party**[Quote management for business organization](https://www.servicenow.com/docs/access?context=quote-management-for-business-location&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)

</td><td>

Multiple sellers or partners can be added to the quote line item for some business orders. There are two types of quote-related parties:

-   Authorized organization: This type of organization partners have full permissions to access, view, edit, or modify quote details
-   Listed organization: This type of organization partners are added solely for tracking purposes and does not have any permissions to view, access, edit, or delete quote details.

</td></tr></tbody>
</table>![Image shows the Quote details form where agents can enter and manage quote information](../image/quote-main-screen-q125.png "Quote Management Details tab")

## Integrate Quote Management with product offering catalogs

Quote Management is integrated with the product catalog and pricing to make adding products to your quote easier and convenient. Agents use the catalog to browse product offerings and the product configurator to add options and pricing to your products. Then they simply add them to the quote. Pricing adjustments that are fetched based on pricing matrices rules are automatically added and presented in the quote.

## Use the product configurator

The product configurator lets your agents configure products in the following ways:

-   Browse and add configurable product offerings from the catalog to create quote lines.
-   Select product options and view product relationships.

The product configurator uses Sales Customer Relationship Management primitives to create and update quote lines and characteristics.

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

## Add cost books in Quote Management

A cost book contains the unit costs for product offerings. Cost books provide your agents with the following benefits:

-   Profit margin calculation: Ability to calculate the profit margin by subtracting the cost price from the quoted selling price, helping your sales team verify that their pricing strategy aligns with desired profit margins,
-   Discount management: Apply discounts to quotes based on cost prices to incentivize bulk purchases or long-term commitments for flexible pricing strategies while maintaining profitability and competitive incentives to your customers.​
-   Negotiation support: Use cost prices as a reference during negotiations with your customers or suppliers. It provides a transparent basis for discussions, helping you build trust and facilitating fair and mutually beneficial agreements.​

To learn more about cost books and their configuration, see [Pricing Management](pricing-management.md), [Create and publish a cost book](../task/create-cost-books.md), [Create a cost book line](../task/create-cost-book-lines.md), and [Configuring Quote Management](configure-quote-management.md).

## Enable a sales agreement in Quote Management

Enabling a sales agreement in Quote Management changes the quote to a sales agreement workflow that sets the products and services according to the sales agreement. Agents can add simple products or configurable products including product bundles to a sales agreement.

-   Configurable bundles with the ability to choose from all available child offers and optional products.
-   Category level discounting
-   Offer level discounting.

## Set a location for product inventories

Use the location feature to set a location for products available in the product catalog.

-   Select a location to add products and services to the quote line.
-   Copy all products and services from one location to another.

## Create PDF documents for a quote

Sales agents can create a PDF document for a quote that can be sent to customers for review and electronic signatures.

-   Quote PDF documents can be linked to electronic signature apps like Docusign that enable customers to sign quotes electronically.
-   Quote PDF document templates can be created that reflect customer branding and logos.
-   Quotes PDF documents that can be sent to customers for review and approvals.

See [Configure quote PDF documents](quote-management-configure-pdf-documents.md) and [Create a quote PDF document](../task/quote-create-pdf-document.md) for more information about creating PDF documents for quotes.

## What to do next

To learn about setting up Quote Management, see [Configuring Quote Management](configure-quote-management.md).

