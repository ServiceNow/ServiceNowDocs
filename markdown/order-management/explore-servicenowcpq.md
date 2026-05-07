---
title: CPQ Configurator
description: The CPQ Configurator interface streamlines the process of configuring and pricing customizable products that are added to Sales Customer Relationship Management transactions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# CPQ Configurator

The CPQ Configurator interface streamlines the process of configuring and pricing customizable products that are added to Sales Customer Relationship Management transactions.

## CPQ Configurator overview

The CPQ Configurator is an attribute-based interface embedded in Sales Customer Relationship Management workflows for opportunities, quotes, orders, and product configuration changes involving sold products and contracts. Product catalog admins use the CPQ Configurator to manage the product configuration experience, while agents and customers use the CPQ Configurator interface to configure customizable products.

-   **Product catalog admin experience**

    Product catalog admins create configurable product offerings using Product Catalog Management. After saving a configurable product, they run a synchronization process that generates an associated blueprint for the product. The blueprint contains all the product attribute values \(also called fields\), product and pricing configuration rules, product relationships, and child products that were defined for the product offering. The blueprint controls the product configuration experience for the product offering and is managed using the CPQ Configurator. When configuration is complete, catalog admins publish the product offering to a product catalog, which also deploys the corresponding blueprint for use.

-   **Agent experience**

    When agents select a configurable product from the product catalog for a Sales Customer Relationship Management transaction, for example when creating an opportunity or quote, the CPQ Configurator opens. The configurator displays the options and features that can be selected. As agents configure the product, a dynamic list of their selections with associated pricing is also displayed.

-   **Customer experience**

    When customers use self-service features, such as placing orders, and select a configurable product from the catalog, the CPQ Configurator launches in the Business Portal. The configurator displays the options and features available for the offering. As customers configure the product, a list of their selections and associated pricing updates dynamically, providing a real-time, accurate view of their customizations.


## CPQ Configurator users

|User|Description|
|----|-----------|
|Product catalog admin|Create configurable product offerings and generate the associated blueprints that contain the attributes \(fields\), product characteristics, product and pricing rules, product relationships, and child products, that guide valid product configuration by agents and customers.|
|Sales and order agents|Add configurable products to opportunities, quotes, orders, and other transactions such as sold products and contracts that involve configurable products in Sales Customer Relationship Management.|
|Customers|Add configurable products for self-service transactions in the Business Portal.|

## CPQ Configurator workflow

The following workflow describes the tasks involved in configuring and using the CPQ Configurator to configure customizable products.

![Workflow that shows the tasks involved in configuring and using the CPQ Configurator, as described in the following steps](../image/configurable-product-offering-setup.svg "CPQ Configurator workflow for generating product blueprints and configuring customizable products")

1.  If upgrading from a release before Zurich, the system admin enables the system property that runs the CPQ Configurator in Sales Customer Relationship Management applications.
2.  The product catalog admin creates and saves a configurable product offering in Product Catalog Management.
3.  The product catalog admin generates the product offering blueprint.
4.  The product catalog admin publishes the configurable product offering so that it’s available in the product catalog and also deployed as a blueprint.
5.  The agent creates a transaction, such as a quote or order in the CSM Configurable Workspace. Or a customer uses the Business Portal for a self-service transaction, for example, placing an order.
6.  The agent or customer selects a configurable product from the product catalog.
7.  The agent or customer configures the product using the CPQ Configurator.
8.  The agent or customer saves and closes the product offering configuration. The product offering is added as a line item for the transaction, such as a quote line or order line item.

## CPQ Configurator benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Generate and maintain blueprints that contain configuration logic \(rules, attributes, product relationships\) for complex products.|[Create configurable product offerings and associated blueprints](../task/som-create-configurable-prod-offerings.md)|Product catalog admins|
|Quickly and accurately configure complex products based on requirements and product attributes, without requiring extensive knowledge of product structure and hierarchies.|[Using the CPQ Configurator](using-servicenowcpq.md)|Sales and order agents, customers|

## What to explore next

To learn more about configuring and using the CPQ Configurator, see:

-   [Configuring CPQ Configurator](configuring-servicenow-cpq.md)
-   [Create configurable product offerings and associated blueprints](../task/som-create-configurable-prod-offerings.md)
-   [Using the CPQ Configurator](using-servicenowcpq.md)
-   Online help \(access Logik help topics in the CPQ Configurator interface for product catalog admins\)

