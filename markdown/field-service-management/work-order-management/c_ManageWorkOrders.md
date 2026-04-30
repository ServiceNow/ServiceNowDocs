---
title: Manage work orders
description: Work orders are requests for off-site work. Users with the appropriate roles create the work orders and provide the necessary information needed for the work order tasks. Then other users qualify those work orders and create the tasks necessary to complete the work order.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Prepare work orders, Using Field Service Management, Field Service Management]
---

# Manage work orders

Work orders are requests for off-site work. Users with the appropriate roles create the work orders and provide the necessary information needed for the work order tasks. Then other users qualify those work orders and create the tasks necessary to complete the work order.

## Creating work orders

If you have the wm\_initiator or wm\_initiator\_qualifier role, you can create work orders. You can create entirely new work orders, or you can create a work order from another record.

Work orders can be created from these other record types: case, incident, change, problem, or project task. They can also be created from another existing work order. For each record, you can create only one work order.

-   **Work orders created from another existing work order**

    If the scope of an existing work order changes during the execution phase, you can create another work order from it. Analyze whether the scope change can be managed by adding additional tasks instead of creating another work order.

    When you create a work order from an existing work order, the following information is copied from the original work order:

    -   Work order record reference \(in the **Initiated from** field\)
    -   Affected CI
    -   Caller
    -   Location
    -   Priority
    -   Short description
    -   Description
    Because some information is copied from the original record, an existing work order can be used as a template to create new work orders.

-   **Work orders created from an incident, problem, change, or project task record**

    If an incident, problem, change record, or project task must be assigned to an off-site agent and tracked, you can create a work order from it. Some information from the original record is copied automatically into the new work order.

<table id="table_b5b_2nk_2r"><thead><tr><th>

Record type

</th><th>

Fields copied to the work order

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

-   Incident record reference \(in the **Initiated from** field\)
-   Caller
-   Location
-   Priority
-   Short description
-   Description
 For more information, see [Integration with Incident Management](../../field-service-management/concept/incident-for-fsm.md).

</td></tr><tr><td>

Case

</td><td>

-   Account
-   Contact
-   Affected CI
-   Location
-   Asset
For more information about creating a work order from the case, see [Work orders in CSM Agent Workspace](https://servicenow.com/docs/bundle/vancouver-field-service-management/page/product/field-service-management/concept/field-service-workspace.html).

</td></tr><tr><td>

Problem

</td><td>

-   Problem record reference \(in the **Initiated from** field\)
-   Affected CI
-   Priority
-   Short description
-   Description


</td></tr><tr><td>

Change

</td><td>

-   Change record reference \(in the **Initiated from** field\)
-   Affected CI
-   Priority
-   Short description
-   Description
 For more information, see [Integration with Change Management](../../field-service-management/concept/change-for-fsm.md).

</td></tr><tr><td>

Project task**Note:** Before work orders can be created from project tasks, Field Service Management must be integrated with Project Portfolio Management

</td><td>

-   Short Description
-   Location
 These work order fields are synchronized with the project task

-   State
-   Scheduled start
-   Estimated end
 For more information about the synchronized fields, see [Integration with Project Portfolio Management](../../field-service-management/concept/project-management-integration.md).

</td></tr></tbody>
</table>    Work orders can be filtered based on different attributes, such as qualification group, location, initiated from, priority, state, and so on. This help to create a group of similar work orders.


-   **[Apply a work order template](../../it-services/task/t_UseTheWorkOrderTemplate.md)**  
Work order templates enable users with the proper roles to automatically create work orders, tasks, and part requirements.
-   **[Create a work order](../task/t_CreateAWorkOrder.md)**  
When off-site work is requested, create a work order to provide information for the agents who fulfill the request. You can create an entirely new work order, or you can create a work order from these other record types: problem, incident, change, or project task. You can also create a work order from another existing work order.
-   **[Example - Create task without qualifying a work order](../../field-service-management/task/example-create-task-in-draft-state.md)**  
Create work order tasks and part requirements for a work order without qualifying a work order, when it is in the draft state.
-   **[Closing work orders and next steps](c_CloseAWorkOrder.md)**  
In Field Service Management, work orders are closed automatically depending on the states of the associated work order tasks. Work orders are closed when all the tasks reach the closed state. It's helpful to understand what happens after an agent closes a work order task.
-   **[Cancel a work order](../task/t_CancelAWorkOrder.md)**  
Cancel a work order if the work is no longer necessary or if it is a duplicate of another work order.
-   **[Delete a work order](../task/t_DeleteAWorkOrder.md)**  
For tracking purposes, you should close or cancel an existing work order that is no longer in use. Closed and canceled work orders are inactive and don't appear on work order lists. Avoid deleting a work order unless you're cleaning up errors, such as duplicate work orders.
-   **[Field Service Management SLAs](c_FieldServiceAutomationSLAs.md)**  
ServiceNow SLAs track the service level provided by groups and individuals.
-   **[Assign work orders for linear assets in Field Service Management](../../field-service-management/concept/managing-linear-assets-fsm.md)**  
In Field Service Management, you can create and view work orders and work order tasks specifically for the inspection of linear assets. This enables you to systematically assess the condition of the assets and take the necessary measures to maintain the reliability and performance of the linear assets.
-   **[Create a work order for the planned work](../../field-service-management/concept/creating-work-orders-from-planned-work.md)**  
Planned work records enable the scheduler to create future, everyday \(on regular basis\), or on-demand work orders based on the associated work schedule.
-   **[Qualify a work order](c_QualifyWorkOrders.md)**  
Work orders must be qualified to ensure that work order tasks are created and assigned. The qualifying process can be automatic or manual.

**Parent Topic:**[Prepare work orders](../../field-service-management/concept/preparing-work-orders.md)

