---
title: Getting started with CPQ
description: Start building configurations with CPQ, the configuration engine that powers ServiceNow CPQ. Learn how blueprints, products, fields, rules, and layouts work together to create guided selling experiences.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Getting started with CPQ

Start building configurations with CPQ, the configuration engine that powers ServiceNow CPQ. Learn how blueprints, products, fields, rules, and layouts work together to create guided selling experiences.

## About CPQ

CPQ delivers a modern, high-performance configuration engine that acts as the “C” in Configure, Price, Quote, enabling organizations to model complex products with clarity, speed, and precision. Built on an attribute-based configuration approach, ServiceNow CPQ simplifies complexity by evaluating product logic through a unified rules framework—allowing sales teams and buyers to configure highly customizable offerings with ease.

At the core of ServiceNow CPQ is a fast, scalable rules processing engine that evaluates configuration inputs in real time. This engine powers dynamic behaviors such as conditional visibility, guided selections, automated calculations, and configuration validation, ensuring every configuration is accurate and actionable.

Configurations are delivered through blueprints—reusable containers that bring together fields, rules, layouts, and configurable products into a cohesive configuration experience. Blueprints make it easy to design, customize, and extend rich UI experiences without code, while providing a consistent structure for managing logic across environments.

Whether used standalone or embedded in eCommerce platforms, Salesforce, or custom applications, ServiceNow CPQ provides a flexible and performant foundation for delivering guided selling experiences, generating bills of materials, and driving downstream processes such as quoting, manufacturing, and fulfillment.

**Tip:** Involving your CSM in the early phases of your CPQ implementation has a direct impact on the success of your project.

## Perspectives

-   Market View: Focuses on the environment: target markets, customer segments, and partner strategies. Success is measured by selling to the right customers at profitable margins.
-   Organizational View: Focuses on internal operations and systems, such as: Marketing and campaign management, CRM and opportunity management, CPQ, Contract management, ERP, fulfillment, billing, and service. Success is measured by operational efficiency, profitability, and repeatability.
-   Sales Rep View: Focuses on day-to-day selling tasks, such as: identifying targets, analyzing product needs, configuring solutions, agreeing on pricing and terms, and packaging deals and closing sales. Success is measured by closing deals efficiently and meeting customer needs.

## Key concepts

Before you start building, familiarize yourself with the foundational terms used in ServiceNow CPQ:

1.  [Configurable Products](configurable_products.md) — product records that launch a configuration when added to a quote.
2.  [Blueprints](blueprints_101.md) — the containers for configuration logic and UX \(fields, rules, and layouts\).
3.  [Fields](fields_101.md) — variables that collect and store data during configuration \(at the header or line level\).
4.  [Rules](rules_101.md) — logic that validates input, sets values, filters options, or computes outputs \(for example, to produce a BOM\).
5.  [Set up layouts](layout_csv_101.md) — the structure and navigation of the buyside UI. Layouts define the end user interface, how fields are arranged on the page, and how the user travels through the configuration experience.
6.  BOM — bill of materials output used for quoting and/or downstream manufacturing/ERP.

## Build your first configuration

Build your first configuration.

-   Upload a sample blueprint using the Matrix Loader. See the [Configure the Matrix Loader](cpq-using-the-matrix-loader.md).
-   Create a configurable product in Salesforce CPQ \(SFDC\) and associate it with your blueprint. See [The CPQ Configurator](understand-the-commerce-logic-engine.md).
-   Launch the configuration experience by adding the product to a quote and verifying that the blueprint-driven UI is working as expected. See [Set up blueprints](blueprints_101.md).

**Related topics**  


[The CPQ Configurator](understand-the-commerce-logic-engine.md)

