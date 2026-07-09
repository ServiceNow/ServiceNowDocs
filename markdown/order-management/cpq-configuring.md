---
title: Configuring ServiceNow CPQ Configurator
description: Learn how to set up products, rules, pricing, and layouts in ServiceNow CPQ using configuration engine. You can define how users select, customize, and validate products during the quoting process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-configuring.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuring ServiceNow CPQ Configurator

Learn how to set up products, rules, pricing, and layouts in ServiceNow CPQ using configuration engine. You can define how users select, customize, and validate products during the quoting process.

## Configuration workflow

The following workflow describes the tasks involved in configuring and using ServiceNow CPQ to configure customizable products when embedded in Sales Customer Relationship Management.

\[Omitted image "configurable-product-offering-setup.svg"\] Alt text: Workflow that shows the tasks involved in configuring and using ServiceNow CPQ, as described in the following steps

1.  If upgrading from a release before Zurich, the system admin enables the system property that runs the configurator in Sales Customer Relationship Management applications.
2.  The product catalog admin creates and saves a configurable product offering in Product Catalog Management.
3.  The product catalog admin generates the product offering blueprint.
4.  The product catalog admin publishes the configurable product offering so that it is available in the product catalog and deployed as a blueprint.
5.  The agent creates a transaction, such as a quote or order, in the CSM Configurable Workspace. Alternatively, a customer uses the Business Portal for a self-service transaction, for example, placing an order.
6.  The agent or customer selects a configurable product from the product catalog.
7.  The agent or customer configures the product using ServiceNow CPQ.
8.  The agent or customer saves and closes the product offering configuration. The offering is added as a line item for the transaction, such as a quote line or order line item.

## Key components of the Commerce Logic Engine

The Commerce Logic Engine is built from modular components that define how products are configured and presented.

|Component|Description|
|---------|-----------|
|Configured products|Salesforce objects that require configuration in ServiceNow CPQ before being added to the Quote Line Editor \(QLE\).|
|Blueprints|Containers for all components needed to render the UI.|
|Fields|Attributes that capture user inputs.|
|Layouts|Define how the configuration UI is displayed.|
|Rules|Ensure products are configured correctly.|
|Sets|Dynamic arrays that adapt to user selections.|
|Product pickers|Menus for selecting products without running the rules engine.|
|Picklist extensions|Extend the capabilities of picklists.|
|Product lists|Display the configuration BOM to the user.|
|Tables and table queries|Store and retrieve supporting data during configuration.|
|Set repeaters|Combine set functionality with flexible layouts.|
|Associated picklist sets|Dynamically sized sets based on menu choices.|
|Field grids|Tabular field groups for structured data entry.|
|Advanced product actions|Scripts to define which line items are sent to the configuration BOM.|
|Twinning|Copies Salesforce quote data into ServiceNow CPQ fields.|
|Enrichments|Scripts that run outside the rules engine during configuration.|
|External connections|Connect to third-party data sources to retrieve configuration data.|

## Build your first configuration

To build your first configuration:

-   Upload a sample blueprint using the Matrix Loader. See [Configure the Matrix Loader](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-using-the-matrix-loader.md).
-   Create a configurable product in Salesforce CPQ \(SFDC\) and associate it with your blueprint, or create a configurable product offering in Product Catalog Management. See [Create configurable product offerings and associated blueprints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-create-configurable-prod-offerings.md).
-   Launch the configuration experience by adding the product to a quote and verifying that the blueprint-driven UI works as expected. See [Set up blueprints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/blueprints_101.md).

## Examples of commerce logic in action

-   **Sales enablement**

    A sales rep enters requirements, such as the number of users. ServiceNow CPQ applies rules and generates a valid configuration instantly, and the results flow into Salesforce CPQ quotes.

-   **Headless eCommerce**

    A customer answers guided questions in a web storefront, ServiceNow CPQ delivers a tailored recommendation, and the customer purchases without sales intervention.

-   **Manufacturing integration**

    A complex product configuration produces both a Sales BOM and a Manufacturing BOM. The Sales BOM passes to Salesforce CPQ, and the Manufacturing BOM flows to ERP for production planning.


