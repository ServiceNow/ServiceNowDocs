---
title: Pricing Management
description: The Pricing Management application enables your organization to set, manage, and optimize pricing strategies for any Sales and Order Management solution. These pricing strategies enable your sales team to generate opportunities, quotes, and orders with accurate and competitive pricing quickly.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Configure, price, quote, Explore, Sales and Order Management]
---

# Pricing Management

The Pricing Management application enables your organization to set, manage, and optimize pricing strategies for any Sales and Order Management solution. These pricing strategies enable your sales team to generate opportunities, quotes, and orders with accurate and competitive pricing quickly.

The Pricing Management application is the foundation of any Sales and Order Management solution. Pricing Management provides various features to implement pricing in your organization.

**Note:** Check your entitlements to determine if you have access to these features.

## Price lists

Price lists define the prices for products and services offered by your organization. Your agents use price lists to find product pricing quickly when creating quotes and capturing orders. Your pricing admins or managers create price lists and add price list lines that define the list price for each of your product offerings. They can also copy a published price list and its price list lines and use the copy to update the pricing or reuse the price list without having to create a new price list.

-   **Support for multiple price lists**

    Pricing Management supports multiple price lists, such as price lists based on currency or customer account. The initial, default price list that you create is based on the currency used, but you can change the default price list used by your agents. For example, you can create account-based price lists that are tailored to the needs and preferences of a specific customer or provide pre-negotiated prices for them. You can set an account-based price list as the default, which is then used by your agents when they create quotes or orders for that particular customer.

    ![Account-based price list for Funco company and the Funco pricing information displayed in a quote for Funco.](../image/price-list-workspace.png "Example of account-based price list")

-   **Pricing methods**

    The pricing method is either a one-time fee or a recurring pricing fee with monthly and annual frequencies. The pricing method is set in product offerings and is displayed in price list lines.


For details on setting up and managing price list features, see [Configuring product pricing](som-managing-product-pricing.md).

## Sales Agreement price lists

If you're using the Sales Agreement feature, a published sales agreement price list is generated automatically when a sales agent creates a sales agreement from a completed quote. The sales agreement price list reflects the final unit price for each product that is captured as part of the sales agreement. The sales agreement price list is valid for the start and end dates specified for the agreement. To learn more about sales agreements, see [Sales Agreement Management](sales-agreement-mgmt.md).

![Sales Agreement Details tab and Price List Lines tab in CSM Configurable Workspace that show a sales agreement price list](../image/sales-agreement-price-list.png "Example of sales agreement price list")

## Cost books

Cost books define the unit cost for product offerings. This information is used in the Quote Management application to provide sales agents with the unit cost, unit margin amount, and unit margin percentage for products in quotes. With this information, your sales agents can perform a simple profitability analysis by subtracting the cost of the product offer from the quoted selling price.

![Quote details tab that shows the cost book used, and quote line item that shows the unit cost and unit margin amount.](../image/costbook-quote-header-line.png "Example cost book in quote details and margins in quote line")

Your pricing admins or managers create a cost book and add a cost book line to set the unit cost for each product offering. They can also copy a published cost book and its cost book lines to revise costs in the cost book \(update the copy\) or reuse a cost book without having to create a new one. For details on setting up cost books and cost book lines, see [Create and publish a cost book](../task/create-cost-books.md) and [Create a cost book line](../task/create-cost-book-lines.md). For information on activating the cost book and cost margin features in Quote Management, see [Configuring Quote Management](configure-quote-management.md).

## Cost-based attribute adjustments

As a pricing admin, you can capture the base cost for a product based on its characteristics, such as model or size, since those attributes can affect the final cost. You can define a cost-based attribute adjustment for a product by specifying a fixed amount or percentage markup or markdown to be applied to all cost books or to selected cost book lines. The base costs are used by the pricing engine to calculate profit margins for products in sales quotes. For more information, see [Create and publish a cost-based attribute adjustment](../task/create-cost-attribute-adjustment.md).

## Price adjustments

In Pricing Management, you can adjust the list price of your products by specifying a markdown or markup fixed amount or percentage, or a price override, based on the following features:

-   **Product attributes**: Define a price adjustment based on product characteristics, such as model or color. For more information, see [Create a product attribute-based pricing adjustment](../task/som-create-pricing-adjustment.md).
-   **Non-product attributes**: Create a price adjustment based on characteristics that aren’t related to a product, such as shipping information or sales channel. For example, you can create a pricing adjustment for customers in a particular region. For details, see [Create a non-product attribute pricing adjustment](../task/som-create-nonprod-attrib-adjustment.md).
-   **Bundled products**: Create price adjustments for product offerings in a bundled product. For example, you might want to specify a markdown amount for certain product offerings in the bundle, because the bundle provides discounted pricing. For more information, see [Create pricing adjustments for bundled products](../task/som-create-bundle-adjustment.md).

## Pricing matrices

Pricing matrices are frameworks for setting conditions in decision rules, which enable you to implement complex pricing adjustments and manage default price list or cost book selection. For instance, if you have multiple price lists, you can use a pricing matrix to specify the conditions that determine the default price list to be applied when agents create a quote or order. Pricing Management offers the following matrices:

-   **Price List Defaulting**: Select the default price list to be used, such as the standard price list or an account-specific price list. For more information on configuring this price list matrix, see [Control the default price list on transaction header or header line](../task/som-control-default-pricelist.md).
-   **Cost Book Defaulting**: Select the default cost book to be used, for example the standard cost book or an account-specific cost book. To learn more about configuring this matrix, see [Control the default cost book on transaction header or header line.](../task/som-control-default-costbook.md)
-   **Standard Price Adjustment**: Apply an adjustment based on context variables that represent non-product attributes, such as shipping location or account. Pricing Management provides certain system-defined, non-product context variables that you can use in this matrix, but you can also create your own custom variables, for example, market segment. Your pricing administrator can work with your administrator to develop custom context variables that can be used in pricing matrixes. For details on configuring these adjustments, see [Create a non-product attribute pricing adjustment](../task/som-create-nonprod-attrib-adjustment.md). For more information on configuring custom context variables, see [Create a custom context variable](../task/som-create-context-variable.md) and [Map a custom context variable to a transaction entity](../task/som-map-variable.md).
-   **Configuration Component Price Adjustment**: Adjust the price of a product when it's sold as part of a product bundle. For details, see [Create pricing adjustments for bundled products](../task/som-create-bundle-adjustment.md).

## Matrix validations

As an admin, you can use system-defined validations or set your own validations to validate rows entered into the decision tables for pricing and product eligibility rule matrices. For more information on these validations, see [Configuring matrix validation rules](configuring-rule-validations.md).

## Pricing plans

Pricing Management provides a default pricing plan that defines the sequence of steps in which pricing calculations and adjustments are applied to determine final product prices. Adjustments include the pricing changes set in the pricing adjustment matrices. You can use the default plan, or you can copy the default plan and customize it by adding or changing the pricing steps to tailor it for your organization. To learn more, see [Configurable pricing plans](configuring-pricing-plan.md).

## Pricing extensions

Pricing extensions are integration points that your administrator can use to customize the pricing engine, giving you the flexibility to use pricing information from external sources or control the pricing engine processing logic. Pricing Management provides these extensions:

-   Select Price List \(DefaultPriceListExtensionPoint\): Change the selection logic for using the default price list on a quote or order header.
-   Select Cost Book \(DefaultCostBookExtensionPoint\): Change the selection logic for using the default cost book on a quote header.
-   Get Product List Price \(ListPriceExtensionPoint\): Get pricing directly from another data source or extend the current price list derivation.
-   Apply Attribute Adjustments \(AttributeAdjustmentExtensionPoint\): Get attribute adjustments from another data source, such as product manufacturers, or extend the current adjustment derivation logic.
-   Get Cost \(CostExtensionPoint\): Get the unit cost for a product offering directly from another data source or extend the current cost book derivation logic.
-   Apply Pricing Adjustments \(PricingAdjustmentsExtensionPoint\): Get pricing adjustments for a product offering from another data source, or extend the pricing engine logic by not relying on the Standard Adjustment and Component Configuration Rule Matrices to get the adjustment values.

To learn more, see [Use extension points in Pricing Management](extension-points-som-pricing.md).

