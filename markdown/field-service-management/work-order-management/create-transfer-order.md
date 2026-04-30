---
title: Create a transfer order
description: Create a transfer order that moves the necessary parts or assets to the correct stockroom or agent location.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage transfer orders, Manage inventory in Field Service Management, Manage work order tasks, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Create a transfer order

Create a transfer order that moves the necessary parts or assets to the correct stockroom or agent location.

## Before you begin

Role required: wm\_agent, wm\_qualifier, wm\_dispatcher, wm\_admin, or [qualifier combination role](../reference/r_UserRoleInstallWFieldSrvMgmnt.md)

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Orders**.

2.  Open a work order.

3.  Open a work order task.

4.  In the **Part Requirements** related list, click a **Number**.

5.  Click **Source Part**.

    The system completes the **Model** field automatically with information from the part requirement. You can select a different model, but it must be a [substitute](https://www.servicenow.com/docs/access?context=t_AddingSubModelsToHrdwModel&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for the requested model. If you click the reference lookup icon \(![Lookup icon.](../image/SearchIcon.png)\) beside the **Model** field, only the selected model and any substitute models that are in stock are listed.

6.  Select a **From Stockroom**.

    -   Only stockrooms that have the model specified are included in the list. If no stockrooms are listed, the part is considered out of stock.
    -   The **From Stockroom** field is auto-populated with a default stockroom location, only if the part is available in the agent's personal stockroom or assignment group stockroom. You can specify a different stockroom location, if needed.
7.  Select a **To stockroom**.

    -   The **To stockroom** field is auto-populated with a default stockroom location. You can specify a different stockroom location, if needed.
    -   To deliver the items to an agent directly and skip the **Received** stage, select a personal stockroom as the destination. If no agent is assigned to the work order task, the transfer order line waits in the **Received** stage until an agent has been assigned.
    -   To use a part without transferring it, select the same non-personal stockroom for both the source and destination stockroom. This action moves the transfer order directly to the **Received** stage and sets the asset state and substate to **In stock - Pending transfer**.
    **Note:** An error occurs if the same personal stockroom is selected for both the source and destination stockroom. In this case, the transfer order line automatically moves to the **Delivered** stage even if no agent is assigned to the work order task.

8.  Specify the **Quantity requested**.

    If the first stockroom you select does not contain sufficient quantity, then repeat steps 2-5 until the entire quantity required is ordered. As you order from stockrooms, the number in the **Reserved quantity** field is updated automatically. When the numbers in the **Reserved quantity** and **Requested quantity** fields on the Part Requirement form match, the system selects the **Sourced** check box. After one transfer order line is requested from the part requirement, you cannot change the part requirement.

9.  Select a **Delivery method**.

    Qualifiers, dispatchers, agents and users with combined roles can specify a delivery method for parts while a transfer order is in the **Draft** stage. The possible delivery options are:

    -   **Standard**
    -   **Overnight**
    -   **Courier**
    -   **Agent Pickup**
10. Click **Submit**.


-   **[Move an asset through the transfer process](create-transfer-order-line-task.md)**  
Use transfer order line tasks to move assets through the shipment or drop-off transfer process.

**Parent Topic:**[Manage transfer orders](../concept/c_TransferOrders.md)

