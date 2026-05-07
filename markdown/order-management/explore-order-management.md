---
title: Order management
description: The Order Management application streamlines the order life cycle from capture to fulfillment. It automates decomposition, enrichment, and orchestration workflows, empowering users to accelerate delivery, reduce fallouts, and manage complex orders efficiently through a unified workspace and customer portal.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-12-04"
reading_time_minutes: 6
keywords: [explore]
breadcrumb: [Explore, Sales Customer Relationship Management]
---

# Order management

The Order Management application streamlines the order life cycle from capture to fulfillment. It automates decomposition, enrichment, and orchestration workflows, empowering users to accelerate delivery, reduce fallouts, and manage complex orders efficiently through a unified workspace and customer portal.

## Order Management overview

Automate and streamline the complex process of capturing and fulfilling customer orders with Order Management, a central hub that connects sales, operations, and technical teams.

-   Order decomposition: Automatically break down a single, complex customer order into smaller, manageable tasks using predefine product catalogs and decomposition rules.
-   Pricing capabilities: Ensure accurate billing with dynamic price lists, pricing matrices, and adjustment features.
-   Order enrichment: Add necessary data to orders post-capture before they're decomposed.
-   Single source of truth: Establish a unified source for all order data, eliminating silos and ensuring real-time consistency for all stakeholders.
-   Jeopardy and fallout management: Proactively flag at risk orders and automate the handling of fulfillment errors to manage issues effectively.

With Telecommunications Service Management \(TSM\) or Technology Provider Service Management \(TPSM\) subscriptions, you can use workflows that help you manage your industry-specific products and services.

## Order Management users

|User|Description|
|----|-----------|
|Customer|Accesses the Business Portal to browse catalogs, place and track orders, raise issues or request changes to orders, or work offline with agents to place orders or request services.|
|Order agent|Engages with customers and helps them place orders.|
|Order fulfillment agent|Monitors the fulfillment process and updates fulfillment tasks such as receiving, reviewing, and processing orders.|
|Order manager|Manages customer and service orders.|
|Order approver|Approves customer orders and ensures order accuracy.|
|Order fulfillment manager|Manages order fulfillment tasks, reviews and approves orders.|
|Order fallout agent|Investigates and diagnoses order fallout issues, eliminates order processing errors, and unblocks blocked orders.|
|Order fallout manager|Oversees order fallout agent and monitors fallout tasks to ensure that order fallouts are being addressed.|
|Process admin|Manages automated Order Management workflows such as order enrichment, order decomposition, jeopardy management, and so|

1.  Process admins create order enrichment flows, decomposition rules, order orchestration plans, and order fallout logic using Workflow Studio and decision tables. Optionally, they also install and configure Jeopardy Management.
2.  Order agent initiates the order life cycle by capturing an order in Order Management.
3.  The fulfillment agent captures additional technical information essential to fulfillment.
4.  The fulfillment manager reviews the order for accuracy and approves the order.
5.  The system creates domain orders \(product, service, and resource orders\) based on the specification relationships set in the product catalog and decomposition rules. If some of the information isn’t available when order decomposition starts, Order Management can stagger the decomposition to create certain orders using the information available at the time. Order tasks and work orders are created and assigned to the fulfillment based on the orchestration logic.
6.  Using the order timeline view and orchestration UI, the fulfillment manager monitors the order status, fallouts, and jeopardy scenarios.
7.  The fulfillment agents fulfill the order. This could involving installing products at customer sites or provisioning services.
8.  After all order tasks are complete and order is closed, the product inventory records are created, which can be used to cater to future customer requests like disconnecting, suspending, or resuming products or services. The system also creates contracts and entitlements against the sold products and services respectively.

## Order Management benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Create and implement enrichment flows that the system applies during order orchestration.|[Configure order enrichment flows using Decision Tables](../task/configure-order-enrichment.md)|Process admin|
|Configure jeopardy management rules to monitor fulfillment tasks ans alert managers when tasks are at risk.|[Configuring Jeopardy Management](configuring-jeopardy-management.md)|Fulfillment managers|
|Detect errors or exceptions during order processing and take corrective actions to improve SLA compliance and expedite order processing.|[Managing order fallout](fallout-management-overview.md)|Fallout agent|
|Create and track orders via the workspace, or import orders from third-party systems.|[Methods of creating orders in Sales Customer Relationship Management](order-capture-methods-som.md)|Order agents|
|Speed up fulfillment with orchestration workflows driven by an advanced product catalog using the order orchestration UI.|[Using the order orchestration UI](orchestration-plans-for-order-fulfillment.md)|Fulfillment agents, fulfillment managers|
|Track orders, prioritize tasks, and allocate resources using Gantt charts to see order status and risks.|[View an order timeline](../task/view-order-timelines.md)|Fulfillment agents, fulfillment managers|
|Boost productivity and reduce manual tasks for changes to confirmed orders.|[Managing inflight order changes and cancellation requests](inflight-order-change-mgt-overview.md)|Order agents, order managers|
|Drive flexibility and efficiency of complex order orchestration by processing domain orders when the required information becomes available.|[Staggered decomposition](staggered-decomposition.md)|Fulfillment agents|
|Enable post-sale support and drive customer satisfaction by effectively managing customers requests for disconnecting, suspending, or resuming products or services.|[Managing post-fulfillment order changes](managing-orders.md)|Order agents|

## Related links

To learn more about configuring and using Order Management, see:

-   [Configuring Order Management](order-mgt-configuring.md)
-   [Using Order Management](using-order-management.md)
-   [Extending Order Management with ServiceNow applications and integrations](order-mgt-integrating.md)
-   [Order Management reference](../reference/order-mgt-reference.md)
-   [Now Assist for Sales Force Automation \(SFA\)](../../now-assist-som/concept/now-assist-for-sales-and-order-management-som.md)

