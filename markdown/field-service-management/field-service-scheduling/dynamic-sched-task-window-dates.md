---
title: Work order task start and end dates
description: Dynamic scheduling uses work order task Window start and Window end dates to schedule tasks.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Assigning work order tasks to agents using dynamic scheduling, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Work order task start and end dates

Dynamic scheduling uses work order task **Window start** and **Window end** dates to schedule tasks.

If both the **Window start** and **Window end** dates are present in the work order tasks, dynamic scheduling uses these dates.

If the task has a **Window start** date but the date has passed, dynamic scheduling uses the current date and time for this value.

If the task has a **Window start** date but no **Window end** date, dynamic scheduling uses the **com.snc.wm.wo.task\_window\_day** property to determine this value.

If the task has no **Window start** date but has a **Window end** date, dynamic scheduling uses the current time for this value.

If the task has neither a **Window start** nor a **Window end** date, dynamic scheduling uses the current time and date for the **Window start** and the **com.snc.wm.wo.task\_window\_day** property for the **Window end**.

If a task is created, the **Window end** date gets automatically populated based on the latest SLA breach date from its parent work order. The business rules **Populate Window End Based On SLA** for both Task SLA \[task\_sla\] and Work Order Task \[wm\_task\] tables, and the client script **Calculate Window End** has to be set to **True**.

If a task is created and **Fixed window** is enabled, the business rules and client scripts doesn't execute and **Window end** time is not updated. If a work order is created based on an appointment and there is an SLA associated with the work order, the **Window end** time is populated based on the appointment and not on the SLA.

**Window start** date gets updated for the work order tasks based on the delivery date of the transfer order only for work orders that are not assigned. The business rule **Sync up Delivery Time with WOT** [business rule](../../planning-and-policy/reference/r_InstalledWithFSM.md) has to be set to **True**. Multiple transfer orders that has mandatory part requirements, the **Window start** is set to the latest delivery time of the transfer order. **Window start** date is only updated based on transfer orders only when the part requirement associated with the transfer order is mandatory. However, you can manually edit the window start time and override the existing date that is populated based on the transfer order.

**Note:** The **Window start** date is not updated if the work order task is:

-   Associated with an appointment
-   Fixed Window
-   Window end is populated and is before the delivery by date

**Parent Topic:**[Assigning work order tasks to agents using dynamic scheduling](../concept/using-dynamic-scheduling.md)

