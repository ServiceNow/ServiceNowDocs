---
title: Closing work orders and next steps
description: In Field Service Management, work orders are closed automatically depending on the states of the associated work order tasks. Work orders are closed when all the tasks reach the closed state. It's helpful to understand what happens after an agent closes a work order task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/c\_CloseAWorkOrder.html
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Closing work orders and next steps

In Field Service Management, work orders are closed automatically depending on the states of the associated work order tasks. Work orders are closed when all the tasks reach the closed state. It's helpful to understand what happens after an agent closes a work order task.

Role required: wm\_agent, wm\_ext\_agent.

Work orders are closed in the following scenarios:

-   If all work order tasks are marked **Closed Complete**, the work order state changes to **Closed Complete**.
-   If at least one work order task is marked **Closed Incomplete**, the work order state changes to **Closed Incomplete**.

After a work order is closed, the time and effort for it are calculated automatically. The work order also becomes inactive and is removed from the list of work orders.

After an order has been assigned to an agent, that agent can complete and close the order under two conditions:

-   When the **Request lifecycle is task driven** configuration option is enabled, all states of the work order are driven by the task. The agent can click the **Close Complete** button on the Work Order Task form to close any tasks that need to be closed manually. After all of the work order's tasks are closed, the work order is closed automatically.
-   When the **Request lifecycle is request driven** configuration option is set and all of the work order's tasks are closed, the agent to whom the work order is assigned can click the **Close Complete** button on the Request form to close and complete the order.

## Example: AI-Generated Work Order Closure Summary

A service technician needs to close a work order quickly without spending time writing detailed summaries from memory. ServiceNow Otto for Field Service Management \(FSM\) analyzes work order task information and generates a structured closure summary that technicians can review, edit, and save before closing the task.

|Step|Actor|Action|
|----|-----|------|
|1|Technician|Logs work performed and parts used|
|2|System|Analyzes work order activity|
|3|System|Generates structured summary|
|4|Technician|Reviews and edits summary|
|5|Technician|Saves summary to work order|
|6|Technician|Closes work order|

