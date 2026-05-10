---
title: Order fulfillment
description: Learn about the order fulfillment process and tools available for monitoring and tracking order tasks so your teams can fulfill orders efficiently, handle exceptions in a timely manner, and drive customer satisfaction.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-10-10"
reading_time_minutes: 5
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Order fulfillment

Learn about the order fulfillment process and tools available for monitoring and tracking order tasks so your teams can fulfill orders efficiently, handle exceptions in a timely manner, and drive customer satisfaction.

## Order fulfillment process

Order fulfillment tasks are the actionable units that drive the completion of domain orders \(product, service, resource\) in Order Management. For each domain order, a subflow is initiated to coordinate its fulfillment. The specific subflow is selected using a decision table \(Product/Service/Resource Order Fulfilment Policy\) based on the type of the domain order. This subflow is responsible for defining order tasks and their dependencies, managing the state of the domain order, and notifying SOM when the tasks are ready for tracking in Jeopardy Management.

1.  Task creation
    -   Order fulfillment tasks are automatically generated as part of the orchestration plan when an order is approved and decomposed into domain orders.
    -   Each domain order \(product, service, resource\) can have multiple associated tasks, created based on product specifications, decomposition rules, and subflow logic.
    -   Order tasks are created in parallel or in sequence, with dependencies managed via subflow configuration.
2.  Task assignment
    -   Tasks are automatically assigned to fulfillment agents or teams responsible for execution using the orchestration logic. Fulfillment managers can manually reassign tasks as needed.
    -   SLA definitions and jeopardy management policies are linked to tasks to monitor progress and flag delays.
3.  Task execution
    -   Fulfillment agents perform the required actions for each task, such as provisioning, configuration, shipment, or installation.
    -   Fulfillment managers track the progress of tasks and domain orders in real time using tools like the timeline view and order orchestration UI, which provide visibility into task status, dependencies, and risk indicators.
    -   Agents update task status, add notes, and resolve issues as they work through the fulfillment steps.
4.  Monitoring and exception handling
    -   Agents periodically monitor the progress of all fulfillment tasks and the overall order.
    -   If a task encounters an issue such as missing information, system error, or delay, it can be escalated or flagged for jeopardy management.
    -   Notifications are sent to relevant stakeholders if tasks are delayed or require attention.
5.  Task completion and closure
    -   After the required actions for a task are completed, agents update the task status to Complete.
    -   Closing all tasks associated with a domain order triggers the closure of the domain order itself.
6.  Order closure
    -   When all fulfillment tasks and domain orders are closed, the overall order is marked as complete.
    -   Final updates are made to the sold products or product inventory, and customer records as needed.

## Tools for tracking order fulfillment

Provide powerful tools to fulfillment agents and managers for monitoring and managing the entire order fulfillment life cycle. The order timeline view and the order orchestration UI enables users to track order line items, domain orders, and order tasks for any given order, all in a single, unified workspace.

The timeline view offers a comprehensive, Gantt-style visualization of all order line items and associated tasks for an order. Fulfillment agents and managers can see the current status of each task, including jeopardy indicators that highlight at-risk items, estimated durations, and dependencies between tasks. This view allows users to quickly assess progress, identify bottlenecks, and take proactive action to expedite fulfillment. By consolidating all relevant information such as order lines, domain orders, and tasks into one interface, agents no longer need to navigate multiple forms or lists, streamlining their workflow and improving operational efficiency. To learn more, see [View an order timeline](../task/view-order-timelines.md).

The order orchestration UI provides a hierarchical, expandable view of how fulfillment tasks are grouped and related by domain helping you to visualize how order line items, domain orders, and order tasks are structured and interconnected. Fulfillment agents and managers can drill down into specific domains or tasks, understand relationships and dependencies, and view summary information such as duration and jeopardy status. The order orchestration UI displays the dependencies between domain orders and order tasks, helping you understand which tasks must be completed before others can begin. You can also view the current state of each associated order line item, domain order, and order task within the hierarchy, making it easy to identify progress, spot bottlenecks, and address issues proactively. This tool is especially valuable for complex orders that span multiple domains, as it clarifies how tasks are sequenced and coordinated. The orchestration UI complements the timeline view by offering deeper insight into the structure and flow of fulfillment activities, empowering users to resolve issues and optimize task execution without losing sight of the broader order context. For more information, see [Using the order orchestration UI](orchestration-plans-for-order-fulfillment.md).

-   **[View an order timeline](../task/view-order-timelines.md)**  
View Gantt chart timelines that display the status of a domain order and order tasks, show dependencies between order tasks, and identify tasks that are in jeopardy.
-   **[Review an order orchestration plan](../task/review-order-fulfillment-orchestration-plan.md)**  
Track the progress of an order in the fulfillment process by reviewing the orchestration plan for the order, its order line items, and domain product, service, or resource orders. By using the order orchestration UI, you can easily identify and resolve any delays or fallouts so that you can do the order fulfillment process more efficiently.
-   **[Review and close fulfillment tasks](../task/order-mgt-customer-order-tasks.md)**  
Review and update the fulfillment tasks that are associated with an order, or order orchestration plan, so that you can make sure that all tasks are properly completed.
-   **[Creation of sold product and product inventory records](order-mgt-sold-product-creation.md)**  
Learn how the Order Management application creates and maintains the customer product and service inventory. By using this application, you can maintain an accurate inventory of your customer products and services.
-   **[Horizontal relationships between products](horizontal-relationships.md)**  
By using a compatibility rule, you can define the horizontal relationships between your product, service, and resource specifications.

**Parent Topic:**[Using Order Management](using-order-management.md)

**Related topics**  


[Manage work orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/c_ManageWorkOrders.md)

