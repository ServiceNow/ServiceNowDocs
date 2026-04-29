---
title: Using Order Management
description: ServiceNow Order Management provides a centralized platform to create and manage customer and service orders throughout their entire life cycle. It automates the complex process from order capture and enrichment through to fulfillment and closure, promoting seamless coordination between sales, operations, and technical teams.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [use]
breadcrumb: [Use, Sales and Order Management]
---

# Using Order Management

ServiceNow Order Management provides a centralized platform to create and manage customer and service orders throughout their entire life cycle. It automates the complex process from order capture and enrichment through to fulfillment and closure, promoting seamless coordination between sales, operations, and technical teams.

## Overview of the order life cycle

Access the Order Management capabilities from the CSM/FSM Configurable Workspace to capture and manage orders. A typical order life cycle is a structured, multiphase process that guides a customer's request from initial submission to final delivery and fulfillment, as shown in the following illustration.

![Order life cycle Infographic showing how to create and manage orders using Order Management. For details, refer to the list of task topics that follows.](../image/using-order-management-landing.svg "Creating and managing orders")

1.  [Creating orders](../task/som-create-product-order.md)

    The order life cycle begins when a customer's request is submitted. This could be from a salesperson creating a quote that's then converted to an order, a sales agent directly capturing an order through the workspace, a customer placing an order online through the Business Portal, or an order being created via an API from another system. This phase focuses on getting all the customer-facing details, including what was ordered, pricing, and customer information, into the system.

2.  [Enriching orders](order-enrichment.md)

    If order enrichment subflow is configured for a product offering, then order enrichment tasks are created. The fulfillment agent captures additional details required to fulfill the order. This phase prevents errors from propagating further into the process. Not all orders need enrichment.

3.  [Approving or rejecting orders](approving-rejecting-orders-som.md)

    The fulfillment manager reviews the order, order lines, and pricing details and approves or rejects the order.

4.  \[System\] [Order decomposition](order-mgt-order-decomposition.md)

    This is a critical step for businesses selling complex products or services. The single, high-level order is automatically broken down into smaller, actionable service orders or fulfillment tasks based on how the process admin has configured order decomposition. For example, a customer's order for a telecom bundle would be decomposed into separate tasks for IT provisioning, a field technician, and the billing department. This process translates the customer's request into a detailed operational plan.

    View product, service, or resource orders for tracking the fulfillment process, verifying that all required tasks and suborders are created correctly, and confirming that the order progresses through its life cycle as expected. For more information, see [View domain orders](../task/view-domain-orders.md).

5.  \[System\] [Order orchestration](order-orchestration.md)

    The system orchestrates the fulfillment of each individual product, service, and resource orders. Tasks are automatically created and assigned to the correct teams and systems, and the application tracks their progress.

    Work orders are created if you have an integration with Field Service Management.

6.  \(Optional\) [Inflight order changes](inflight-order-change-mgt-overview.md)

    Inflight order changes come into the picture after an order has been submitted and is actively being processed, but before it has been completely fulfilled and closed. These changes are a form of MACD orders \(Modify, Adds, Changes, and Deletes\) that occur during the fulfillment life cycle.

7.  [Order fulfillment](reviewing-orchestration-plans-order-fulfillment.md)

    Fulfillment agents complete order tasks assigned to them. Fulfillment managers monitor the fulfillment process and manage issues using features such as Jeopardy Management to alert teams about potential delays and Fallout Management to handle errors.

    As each fulfillment task is completed, the service or product is activated or delivered to the customer. This can involve anything from a physical delivery to the electronic provisioning of a digital service. Once all products and services are activated and delivered, the order is officially closed. The system updates the order status to reflect completion and updates creates sold product records.

8.  [Managing order fallouts](fallout-management-overview.md)

    Manage failures that may take place during order fulfillment due to errors and exceptions. These exceptions include incorrect data, connectivity problems, inadequate inventory supply, or other unforeseen issues.

9.  [Monitoring order jeopardy](../task/monitoring-jeopardy-management.md)

    Proactively monitor and mitigate order delivery delays, dynamically track task progression to predict potential order fulfillment delays, and alert service delivery teams when fulfillment plans exceed or are expected to exceed committed completion times by monitoring the jeopardy status.

10. [Managing post-fulfillment order changes](managing-orders.md)

    Order agents can make the following post-sale changes to the orders after an initial order has been placed and fulfilled:

    -   Change
    -   Disconnect
    -   Suspend
    -   Resume

**Related topics**  


[Configuring Order Management](order-mgt-configuring.md)

[Order types in Sales and Order Management](som-order-types.md)

[Action types for customer and service orders](order-mgt-customer-order-types.md)

[Order life cycle states](order-lifecycle-states.md)

[Methods of creating orders in Sales and Order Management](order-capture-methods-som.md)

[Reviewing customer or partner accounts](reviewing-customer-accounts.md)

[Now Assist for Order Management](../../now-assist-order-mgmt/concept/now-assist-order-management.md)

[Order Management reference](../reference/order-mgt-reference.md)

