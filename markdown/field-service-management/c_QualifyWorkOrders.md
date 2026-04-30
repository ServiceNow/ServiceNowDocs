---
title: Qualifying work orders
description: Work orders must be qualified to ensure that work order tasks are created and assigned. The qualifying process can be automatic or manual.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing work orders, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Qualifying work orders

Work orders must be qualified to ensure that work order tasks are created and assigned. The qualifying process can be automatic or manual.

Depending on how the [Qualification is required for new requests](../task/t_ConfigureFieldService.md#LifecycleOptions) option is set in the Field Service Management configuration, the qualifying process is manual or automatic.

-   **Manual qualification**

    When **Qualification is required for new requests** is enabled, the qualifying process is manual. Each work order must go through these states of the process:

    **Awaiting Qualification** &gt; **Qualified**

    In the Awaiting Qualification state, all the work order tasks must be qualified by a user with the appropriate role.

    Qualifiers, who are users with the wm\_qualifier role, select the dispatch group, add work order tasks, and define part requirements. Qualifiers can also edit the affected CI, short description, and description for work orders.

    After all the tasks are qualified, the work order is moved to the Qualified state.

    Work orders tasks can be qualified individually or in bulk.

-   **Automatic qualification**

    When **Qualification is required for new requests** is disabled, the qualifying process is automatic. The work order is automatically qualified and moved directly to the next state that is configured for Field Service Management.

    A task is also automatically created for each qualified work order. These work order tasks are automatically qualified but must still be manually moved to the dispatch queue. Users with the wm\_initiator\_qualifier or wm\_admin roles can move the work order tasks.


## Filtering available dispatch groups

The **work.management.limit.location** property controls whether the choice list of available dispatch groups is filtered by proximity to the task location.

-   **[Request additional information to qualify a work order](../task/t_RequestAdditionalInformation.md)**  
Transfer orders move necessary parts to the location where the agent can receive them. If there is not enough information to create a transfer order, the dispatcher can request more details from the qualifier.
-   **[Qualify a work order](../task/t_QualifyATask.md)**  
When a work order is assigned to you for qualification, review and qualify its tasks to ensure that they contain enough information for the groups that are dispatched to work on them. Qualifying work order tasks is required only when Field Service Management is configured for manual qualification.
-   **[Move a work order task to the dispatch queue](../task/t_PromoteDraftWorkOrderTasks.md)**  
If Field Service Management is configured to automatically qualify work orders, tasks are also automatically created for the orders. When one of these automatically created tasks is assigned to you, select a dispatch group for it and move it to the dispatch queue.

**Parent Topic:**[Managing work orders](c_ManageWorkOrders.md)

