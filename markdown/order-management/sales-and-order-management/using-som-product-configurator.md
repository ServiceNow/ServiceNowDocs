---
title: Using the legacy product configurator
description: The legacy product configurator in Sales Customer Relationship Management is an interface for customizing configurable product offers. The interface displays the product options available and automatically calculates product pricing as you select options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/sales-and-order-management/using-som-product-configurator.html
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-15"
reading_time_minutes: 1
breadcrumb: [Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Using the legacy product configurator

The legacy product configurator in Sales Customer Relationship Management is an interface for customizing configurable product offers. The interface displays the product options available and automatically calculates product pricing as you select options.

## Legacy product configurator interface

\[Omitted image "l2c-configurator-callouts-2.png"\] Alt text: Interface for adding configurable products that has sections for navigating the product hierarchy, selecting product and characteristic options, and reviewing the current selection with pricing

The interface consists of three main sections:

-   **Product hierarchy**: Lists the parent and child product relationships for configurable products.
-   **Option selection**: Displays the product options that can be selected, for example product characteristics such as color or model.
-   **Current Selection**: Shows the pricing for the options that you select. The pricing is calculated automatically and displayed dynamically as you select product options.

When you complete the product offering configuration, select **Add** to add the product as a line item for the transaction.

## Selecting complex product characteristics and options

When you select a complex product for opportunities, quotes, and orders, the product hierarchy and option selection sections in the configurator display the complex attributes and options hierarchically.

You can expand the product hierarchy to show the available characteristics and options. The gear icon \[Omitted image "gear\_icon.png"\] Alt text: displayed next to a child product indicates that a hierarchy of complex characteristics is available at that level. Select that level to view the characteristics and options.

**Note:** Pricing details aren’t provided in the **Current Selection** pane for complex characteristics.

\[Omitted image "complex-char-configUI-order.png"\] Alt text: Product configurator interface showing the gear icon that identifies hierarchical product characteristics available

-   **[Create multiple configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/create-multiple-child-configs.md)**  
Create multiple configurations of a child product offering when you're adding a configurable product to an opportunity, quote, or order. You can then configure the product options and characteristics separately for each offering configuration.

**Parent Topic:**[Using configure, price, quote applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/using-cpq.md)

