---
title: Closing work orders
description: In Field Service Management, work orders are closed automatically depending on the states of the associated work order tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing work orders, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Closing work orders

In Field Service Management, work orders are closed automatically depending on the states of the associated work order tasks.

Role required: wm\_agent, wm\_ext\_agent.

Work orders are closed in the following scenarios:

-   If all work order tasks are marked **Closed Complete**, the work order state changes to **Closed Complete**.
-   If at least one work order task is marked **Closed Incomplete**, the work order state changes to **Closed Incomplete**.

After a work order is closed, the time and effort for it are calculated automatically. The work order also becomes inactive and is removed from the list of work orders.

After an order has been assigned to an agent, that agent can complete and close the order under two conditions:

-   When the **Request lifecycle is task driven** configuration option is enabled, all states of the work order are driven by the task. The agent can click the **Close Complete** button on the Work Order Task form to close any tasks that need to be closed manually. After all of the work order's tasks are closed, the work order is closed automatically.
-   When the **Request lifecycle is request driven** configuration option is set and all of the work order's tasks are closed, the agent to whom the work order is assigned can click the **Close Complete** button on the Request form to close and complete the order.

**Parent Topic:**[Managing work orders](c_ManageWorkOrders.md)

