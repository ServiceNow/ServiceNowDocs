---
title: ServiceNow CPQ Configurator
description: The ServiceNow CPQ Configurator is an advanced commerce logic solution that allows businesses to configure and sell products more effectively. Unlike traditional product-based systems, ServiceNow CPQ uses an attribute-based configuration model. This ensures that users are guided through selections, rules are enforced automatically, and only valid outcomes are generated.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-29"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# ServiceNow CPQ Configurator

The ServiceNow CPQ Configurator is an advanced commerce logic solution that allows businesses to configure and sell products more effectively. Unlike traditional product-based systems, ServiceNow CPQ uses an attribute-based configuration model. This ensures that users are guided through selections, rules are enforced automatically, and only valid outcomes are generated.

The configurator connects customers to products faster and easier by enabling:

-   Attribute-based user inputs that drive the commerce logic engine.
-   Guided product and solution recommendations.
-   Headless eCommerce experiences integrated with existing channels.
-   No-code/low-code tools for simplified maintenance and administration.

## Key benefits

-   Faster sales cycles: Guided Selling and Solution Selling that reduces errors. Customers and sales reps can configure products quickly and confidently.
-   Next-Generation Performance: High-performance architecture supports large product models. Flexible UI built with Salesforce Lightning for seamless user experience.
-   Accelerated Product Launches: Introduce products faster with fewer SKUs to manage. Quickly deploy and update rules across channels.
-   Lower Administration Costs: A no-code/low-code Admin interface consolidates multiple systems. Reduces integration complexity and ongoing maintenance overhead.

## Key capabilities

-   Attribute-Based Configuration: Prompts users with guided questions. Applies configuration rules to ensure valid results. Eliminates human error found in product-based systems.
-   Guided Selling and Headless eCommerce: Self-service buyers receive automated recommendations. Sales reps follow consistent workflows.
-   Dynamic Bills of Materials \(BOMs\): Sales BOMs integrate with Salesforce CPQ Quote Line Editor. Manufacturing/custom BOMs support ERP and Order Management flows.
-   No-Code/Low-Code Administration: Intuitive UI for creating, updating, and deploying rules. Removes dependency on IT or development teams.
-   High-Performance Architecture: Handles complex configurations at scale. Maintains speed without compromising accuracy.

## Product-based and attribute-based configuration

Product-Based Configuration

-   Requires sales reps to manually select products.
-   High risk of error due to changing lists and rules.

Attribute-Based Configuration

-   Prompts users with questions about desired features.
-   Applies configuration rules to automatically generate valid outputs.
-   Results can be quoted in Salesforce CPQ or purchased directly online.

## Examples of commerce logic in action

-   Sales Enablement
    -   Sales rep enters requirements \(e.g., “number of users”\).
    -   ServiceNow CPQ applies rules and generates a valid configuration instantly.
    -   Results flow into Salesforce CPQ quotes.
-   Headless eCommerce
    -   Customer answers guided questions in a web storefront.
    -   ServiceNow CPQ delivers a tailored recommendation.
    -   Customer purchases without sales intervention.
-   Manufacturing Integration
    -   Complex product configuration produces both a Sales BOM and Manufacturing BOM.
    -   Sales BOM passes to Salesforce CPQ.
    -   Manufacturing BOM flows to ERP for production planning.

## Key components

The Commerce Logic Engine is built from modular components that define how products are configured and presented.

|Component|Description|
|---------|-----------|
|Configured Products|Salesforce objects that require configuration in ServiceNow CPQ before being added to QLE.|
|Blueprints|Containers for all components needed to render the UI.|
|Fields|Attributes that capture user inputs.|
|Layouts|Define how the configuration UI is displayed.|
|Rules|Ensure products are configured correctly.|
|Sets|Dynamic arrays that adapt to user selections.|
|Product Pickers|Menus for selecting products without running the rules engine.|
|Picklist extensions|Extend the capabilities of picklists.|
|Product Lists|Display the configuration BOM to the user.|
|Tables and Table Queries|Store and retrieve supporting data during configuration.|
|Set Repeaters|Combine set functionality with flexible layouts.|
|Associated Picklist Sets|Dynamically sized sets based on menu choices.|
|Field grids|Tabular field groups for structured data entry.|
|Advanced Product Actions|Scripts to define which line items are sent to the Config BOM.|
|Twinning|Copies Salesforce Quote data into ServiceNow CPQ fields.|
|Enrichments|Scripts that run outside the rules engine during configuration.|
|External Connections|Connect to third-party data sources to retrieve configuration data.|

