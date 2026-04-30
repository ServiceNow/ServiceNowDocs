---
title: Product configurator
description: The product configurator is a user interface that is embedded in various Sales Customer Relationship Management applications, such as the Opportunity, Quote, and Order Management applications, enabling agents to configure complex products or services dynamically according to customer requirements.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-03-27"
reading_time_minutes: 2
breadcrumb: [Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Product configurator

The product configurator is a user interface that is embedded in various Sales Customer Relationship Management applications, such as the Opportunity, Quote, and Order Management applications, enabling agents to configure complex products or services dynamically according to customer requirements.

**Note:** Check your entitlements to determine if you have access to this feature.

The interface consists of three main sections:

-   **Product hierarchy**: Lists the parent and child product relationships for configurable products. Product hierarchies are configured using relationships and relationship groups. These hierarchies help agents navigate the product at different nodes or levels within a nested bundle. To learn more about how to configure this section of the product configurator, see [Create product offering relationships](../task/som-product-config-offering-relationships.md).
-   **Option selection**: Displays the product options or product characteristic options that can be selected. Characteristics and characteristic options are configured as you build your product offerings and appear in the product configurator. As your agents use the interface, visual indicators, alert messages, and contextual information about their entries are also displayed to help agents complete the order. For more information on configuring these options, see [Create product characteristics and characteristic options](../task/som-product-config-add-characteristics.md).
-   **Current selection**: Shows the pricing for the options that you select, which are calculated automatically and displayed. Pricing for selected options is shown and grouped as bundles as applicable. Also shown are the subtotals and total based on the recurring and one-time pricing methods. See [Configuring product pricing](som-managing-product-pricing.md) for more information.

As an admin, you can use product configurator extension points and methods provided with the Open state management framework to customize the product configurator interface. To learn more about the framework, see [Open state management](som-open-state-management-model.md).

![The image shows the configurator UI with the Product Hierarchy, Option Selection, and Current Selection sections highlighted.](../image/l2c-configurator-callouts-2.png "Product configurator interface")

