---
title: Enriching an order in Order Management
description: As an order agent, capture all the required information for an order before the order approval stage so that there won't be any delay or fallout in the order fulfillment due to missing or incorrect information.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow scenarios, Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Enriching an order in Order Management

As an order agent, capture all the required information for an order before the order approval stage so that there won't be any delay or fallout in the order fulfillment due to missing or incorrect information.

## Overview

An order enrichment process is a set of tasks to capture additional order details by the order agent from your customer.

In the current enhanced order capture process, the agent first captures the basic order details to make the order entry in the Order Management system. Before approving the order, the order agent connects with the customer to get all the required order details according to the customer's business needs.

## How the order enrichment process works

It isn’t required to enrich all the orders. If it is a complex product or service order, the agent decides to enrich the order.

![Infographic displaying the order enrichment flow. For the image description, refer to the text that follows.](../image/order-mgt-enrichment-process.png "Order Enrichment flow")

An order agent creates an order in Order Management by capturing the basic order details and the order **State** field is set to Draft. When the order agent submits the order, the system checks for each order line item whether it requires enrichment or not according to the defined Order Enrichment Flow Policy in the decision table.

![Infographic displays the decision table for order enrichment process](../image/order-mgt-enrichment-decision-table.png "Decision table for Order enrichment process")

If any order line item is applicable for the enrichment process, the state of the order including its line items changes to Enrichment in progress and the Order Enrichment Flow Policy is triggered. The flow creates order enrichment tasks for those order line items. If the line item is not eligible for enrichment, the line item state changes to New.

The order agent reviews and closes each task after providing the required additional details for order decomposition. When the order enrichment is completed, the state of the order line items changes to New from Enrichment in Progress and the order state also changes to New.

The order agent can now approve or reject the order.

