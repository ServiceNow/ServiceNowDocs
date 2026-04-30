---
title: Blueprints, fields, rules, layouts, and BOMs
description: Learn how the core building blocks of ServiceNow CPQ—Blueprints, Fields, Rules, Layouts, and Bills of Materials \(BOMs\)—work together to power configuration and transaction experiences.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-29"
reading_time_minutes: 1
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Blueprints, fields, rules, layouts, and BOMs

Learn how the core building blocks of ServiceNow CPQ—Blueprints, Fields, Rules, Layouts, and Bills of Materials \(BOMs\)—work together to power configuration and transaction experiences.

## Blueprints

Blueprints define the configuration model for a product or offering. They include all the attributes, rules, and user experiences required to guide users through selection and configuration.

-   Each blueprint represents a distinct configurator.
-   Blueprints connect directly to transaction workflows through Transaction Manager.
-   A blueprint includes: fields, rules, layouts, and optional BOM definitions.

## Fields

Fields are attributes that capture data during configuration and transaction workflows.

-   Transaction-level fields capture header data such as customer details, dates, or totals.
-   Line-level fields appear in the transaction grid for products, pricing, and discounts.
-   Field types include text, number, Boolean, picklist, and date/time.
-   Some fields are system-provided. You can also create custom fields for your sales process.

## Rules

Rules automate logic and calculations. Each rule includes:

-   Conditions that define when the rule should run.
-   Actions that define what happens when conditions are met \(set values, hide fields, filter picklist options, display messages\).
-   Rules that can run at transaction level or line level.

You can group rules into rule groups and assign them to stages or events.

## Layouts

Layouts define the user interface for the buyside experience. Layouts let you streamline the UI for different audiences while maintaining consistent logic. They specify:

-   how transaction and line-level fields appear on the page
-   which fields or sections are visible for each stage or persona
-   UI effects, such as messages or highlights triggered by rules

## BOMs

Bills of materials \(BOMs\) translate configured data into structured outputs that integrate with downstream systems.

-   Sales BOMs: Line items that pass into Salesforce for quoting.
-   Manufacturing or custom BOMs: Detailed component structures exported to ERP or fulfillment systems.
-   BOMs ensure that attribute-based configuration outputs map correctly into orderable and manufacturable items.

## How components interact

-   Blueprints bring together fields, rules, layouts, and BOM definitions into a complete model.
-   Fields collect the data users provide.
-   Rules validate input, enforce logic, and calculate outputs.
-   Layouts deliver the tailored UI experience to users.
-   BOMs package the result into line items for quoting and manufacturing.

