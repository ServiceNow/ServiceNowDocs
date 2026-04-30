---
title: Configurable products
description: Learn how configurable products connect blueprints to end-user configuration experiences in ServiceNow CPQ, supporting both headless and Salesforce-integrated use cases.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ Configurator, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Configurable products

Learn how configurable products connect blueprints to end-user configuration experiences in ServiceNow CPQ, supporting both headless and Salesforce-integrated use cases.

Configurable products act as the bridge between a ServiceNow CPQ blueprint and the configuration experience that end users interact with. They define how a specific product launches and behaves during configuration—whether accessed through a headless application or integrated with Salesforce CPQ.

Each configurable product ties together the technical definition of a product \(its blueprint\) with the business object that represents it \(the Salesforce Product2 record or headless configuration record\). This association allows users to configure products dynamically, ensuring that all logic, pricing, and visualization rules from the blueprint are applied in real time.

## Key benefits

Configurable products simplify the connection between your product definitions and customer-facing configuration workflows. They provide:

|Benefit|Description|
|-------|-----------|
|Unified Configuration Launch|Connects each product directly to a ServiceNow CPQ blueprint so the correct configuration UI opens automatically for the end user.|
|Cross-Platform Flexibility|Supports both headless and Salesforce CPQ environments with consistent configuration experiences.|
|Reduced Maintenance|Allows multiple Salesforce Product2 records to link to a single blueprint, simplifying updates across similar products.|
|Faster Go-to-Market|Eliminates the need for custom integration scripts to launch configuration sessions.|

## Configurable product architecture

At a conceptual level, configurable products establish the relationship between your ServiceNow CPQ blueprints and the user-facing configuration layer. This relationship varies slightly depending on whether your environment is headless or Salesforce-integrated:

-   Headless: The configurable product is defined directly in ServiceNow CPQ, and end users access the configuration experience through a front-end application or API connection.
-   Salesforce Integrated: The configurable product acts as the “front door” to the configuration experience in Salesforce CPQ. When users select a ServiceNow CPQ - enabled product, the corresponding configuration UI launches automatically.

In both cases, the configurable product ensures a seamless connection between the product’s logic and its visual configuration experience.

## Salesforce setup

In Salesforce-integrated environments, configurable products link ServiceNow CPQ blueprints to Salesforce Product2 records. This association ensures that selecting a Salesforce product automatically launches the correct ServiceNow CPQ configuration experience.

Only one blueprint can be associated with each configurable product, but multiple Product2 records may link to the same blueprint—simplifying management for similar product variations.

The setup process depends on your Managed Package version used for ServiceNow CPQ: Once configured, selecting the product in Salesforce CPQ automatically opens the ServiceNow CPQ configuration experience for the user.

## Best practices

-   Maintain consistent blueprint naming conventions to simplify identification and mapping.
-   Use CSV uploads for bulk creation of configurable products in headless environments.
-   Verify that Product2 records in Salesforce are ServiceNow CPQ enabled before associating blueprints.
-   Use sandbox environments to validate blueprint mappings before deployment to production.
-   Regularly review configurable product associations when blueprints or product structures change.

**Related topics**  


[Setting up configurable products](configurable_products.md)

