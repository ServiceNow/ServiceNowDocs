---
title: Source parts for work order tasks
description: Source parts from your preferred stockrooms or assignment groups to ensure work order tasks are completed promptly.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Part requirements, Manage inventory in Field Service Management, Manage work order tasks, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Source parts for work order tasks

Source parts from your preferred stockrooms or assignment groups to ensure work order tasks are completed promptly.

## Before you begin

Role required: wm\_agent, wm\_qualifier, wm\_dispatcher, wm\_admin, or [qualifier combination role](../../planning-and-policy/reference/r_UserRoleInstallWFieldSrvMgmnt.md)

## About this task

You can source parts for the work order task either manually or automatically.

-   Automatic process: If the task is assigned to an agent who has the required parts in their preferred stockroom, the part requests are automatically sourced without any manual intervention.
-   Manual process: In case any required part isn’t available in the preferred stockroom, as an agent, you can manually source it from assignment groups or other stockrooms.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Orders Tasks**.

2.  Open a work order task.

    **Note:** Open a work order task that is in **Assigned** state. When a task is assigned to an agent the part requests are automatically sourced from their preferred stockroom if it has the parts. If any part isn’t available in the preferred stockroom, then agents can manually source from the assignment groups or stockrooms.

3.  In the **Part Requirements** tab, you can view a list of required parts for the task.

4.  To source parts manually, do the following:

    1.  Select the part requirement and select the parts that you want to source manually.

        The part requirement page displays all the relevant details.

    2.  Select **Source Part**.

    3.  Select the appropriate option based on the desired sourcing criteria.

    4.  Select **Submit**.

5.  Select **Source Part** and complete the transfer order.

    The transfer order line is created.


## What to do next

Complete the transfer orders: If the agent sources parts from other stockrooms or assignment groups, a transfer order line is created automatically. You can then complete the transfer order, ensuring the parts are moved to the designated location.

**Parent Topic:**[Part requirements](../../planning-and-policy/concept/c_PartRequirements.md)

