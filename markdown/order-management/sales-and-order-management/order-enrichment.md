---
title: Enriching orders in Order Management
description: Order enrichment is a post-capture stage in the Order Management life cycle that enables fulfillment agents to gather additional information from customers for complex orders before submitting the order for approval.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-30"
reading_time_minutes: 2
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Enriching orders in Order Management

Order enrichment is a post-capture stage in the Order Management life cycle that enables fulfillment agents to gather additional information from customers for complex orders before submitting the order for approval.

## Overview of post-capture order enrichment

The order enrichment process is designed to improve fulfillment accuracy and help prevent potential delays or fallouts for complex product or service orders. Fulfillment agents collect additional, context-specific information from customers that is not required during initial order capture because these details don't affect product selection or pricing. The order enrichment process helps the order agents to create basic order entries quickly without needing to wait for technical details that are crucial for fulfillment.

Not all orders require enrichment. For complex offerings such as elevator installations, critical details like installation location and door configuration may not be available during initial order placement. Capturing this information later helps the fulfillment agents to have the necessary data for executing the order efficiently and accurately.

## How the order enrichment process works

After an order is captured by an order agent, the system checks whether the Order Enrichment Flow Policy is configured for the product or service in the decision tables. If the Order Enrichment Flow Policy is configured, enrichment tasks are automatically created against the order lines that require enrichment and are assigned to the appropriate fulfillment agent. At this stage, the state of the order and its line items change to Enrichment in progress. If an order line doesn't qualify for enrichment, it's state changes to New.

Next, the agent then contacts the customer to collect the required details and captures them using the configurator UI. For example, if a customer orders elevators, the fulfillment agent must know the following site details before they send out install technicians:

-   Door configuration \(for example, side-opening, center-opening\)
-   Building entrance width
-   Electrical rating

Only the information necessary for fulfillment is displayed in the configurator UI and stored in the order record.

The fulfillment agent reviews and closes each task after capturing the required additional details for order decomposition and fulfillment. When the order enrichment is completed, the state of the order line items and the parent order changes to New.

The fulfillment agent or manager can now approve or reject the order.

## Benefits

-   Improved accuracy: Reduces delays or fallouts caused by incomplete or incorrect data.
-   Higher conversion rates: Enables customers to place orders quickly without needing all technical details upfront.
-   Operational efficiency: Ensures that fulfillment agents have the correct data at hand.
-   Customer engagement: Builds trust through multi-step collaboration rather than one-time transactions.

## Configuration requirements

Order enrichment tasks are only created if the enrichment process is explicitly configured in the Order Enrichment Flow Policy in the decision tables for a product or service offering. This process ensures that enrichment is applied selectively and only when necessary. For more information, see [Configure order enrichment flows using Decision Tables](../task/configure-order-enrichment.md).

