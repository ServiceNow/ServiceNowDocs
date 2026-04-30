---
title: Transaction Manager
description: Set up, govern, and troubleshoot Transaction Manager so sales teams can capture non-configuration commercial data—such as contacts, addresses, quotes, discounts, and presentation options—alongside ServiceNow CPQ configuration outcomes.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager

Set up, govern, and troubleshoot Transaction Manager so sales teams can capture non-configuration commercial data—such as contacts, addresses, quotes, discounts, and presentation options—alongside ServiceNow CPQ configuration outcomes.

As a transaction administrator, you can

-   Access stages, associated fields, related rules, rule groups, events, layouts, views, and personas.
-   Decide the sales workflow stages you need and what must be true to enter each stage \(entry criteria\).
-   Identify transaction-level \(header\) fields and transaction-line fields you’ll capture.
-   Enable these optional pilots:
    -   Transaction Converse for natural-language line-item operations
    -   Cosmo SmartPredict for in-context predictive recommendations

## How Transaction Manager is organized

In Admin, choose the transaction context in the top navigation. The left menu exposes Transaction Manager admin areas \(stages, associated fields, related rules, rule groups, events, layouts, views, and personas\). The main work area changes based on the entity you’re editing.

Core building blocks and relationships include:

-   Stages that structure the sales process. Each stage may have entry criteria and can invoke rule groups and events. A transaction is in one stage at a time.
-   Fields that store data. Use transaction-level \(header\) fields for deal metadata and line-level fields for the grid of items and pricing.
-   Rules that evaluate conditions and perform actions such as hiding, messages, including or excluding picklist values, and setting or clearing values. Use rule groups to bundle rules and attach them to stages and events.
-   Events such as buttons and API triggers that can run rule groups and drive stage transitions.
-   Layouts and UI effects that define the buyside experience.
-   Views and personas that tailor the layouts and fields that appear for a particular audience or stage.

    **Note:** Favor many simple, non-scripted rules; the rules engine can evaluate tens of thousands quickly and automatically optimizes their order. To keep the UI responsive, avoid scripting where you can.


