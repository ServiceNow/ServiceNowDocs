---
title: Order Management data model
description: The Order Management data model provides a framework that enables you to capture, manage, orchestrate, and fulfill customer orders and external service orders for products and services.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Order Management data model

The Order Management data model provides a framework that enables you to capture, manage, orchestrate, and fulfill customer orders and external service orders for products and services.

## Order life cycle

In Order Management, a customer order moves through the various stages of an order's life cycle.

|Stage|Description|
|-----|-----------|
|Customer order|Main order entity that is captured and created for managing the end-to-end life cycle of a customer request for products or services.|
|Enrichment|Additional information that is required for the order decomposition and for the fulfillment process. Attributes and elements can be added to orders that are required for downstream applications, such as billing or activation.|
|Decomposition|Order that is split into multiple suborders for fulfillment.|
|Orchestration|Order fulfillment coordination that uses a fulfillment flow.|

## Order enrichment and decomposition process

A customer order can have one or more order line items. The enrichment and decomposition process creates the required product, service, and resource order for each order line item, using the specification relationship information in the Product Catalog. The following diagram is an example of how a customer order can be enriched and decomposed.

![Infographic displaying the enrichment and decomposition process of customer order. For the image description, refer to the text that follows.](../image/order-mgt-decomposition.png "Order enrichment and decomposition process")

The fulfillment plan uses decision tables to match the flow for a product order. The assigned flow then triggers the required order fulfillment tasks.

The following diagram shows how the fulfillment process works for a telecommunications product order.

![Infographic displaying the customer order review, approval, and decomposition process.](../image/som-om-workflow-2.png "Order fulfillment workflow example")

