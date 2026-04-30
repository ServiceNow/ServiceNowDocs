---
title: Instantiating your network inventory by using design and assign
description: By instantiating your network inventory in the Telecommunications Network Inventory application, you can generate and validate your inventory records at the site level. You can also generate your individual network instances from your defined inventory templates and models and then verify that they’re properly configured.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Instantiating your network inventory by using design and assign

By instantiating your network inventory in the Telecommunications Network Inventory application, you can generate and validate your inventory records at the site level. You can also generate your individual network instances from your defined inventory templates and models and then verify that they’re properly configured.

## Design and assign overview

You can instantiate a network inventory by using the design and assign function by doing the following tasks:

1.  Create a change request by using the change model.

    A change request records the details about the change, such as the reason of the change in any network, priority, risk, type of change, and change category. By using a change request, you can change any existing network workflow. You can also expand the application capabilities, request new services, modify network structures, and much more. To learn more, see [Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md).

2.  Execute a change task.

    The list of tasks are created from a change-triggered workflow or you can create a change task manually. The change tasks help you to track and manage the various tasks required to implement the requested changes. By using a list of change tasks, you can assign a task to an inventory agent who can then execute the actions and create a configuration item. At the same time, other agents can work on their assigned change tasks. After all tasks are completed and closed by the agents, the change request can also be closed with comments. To learn more, see [Create and execute a change task in Telecommunications Network Inventory](../task/create-change-task-in-tni.md).


## Using a record producer in the design and assign function

If a record producer form is assigned to the selected change model, based on the provided input, a change request is automatically generated. If a record producer form isn’t assigned, you can assign a record producer. To learn more, see [Assign a record producer form to a change model](../task/create_record_producer_form_for_a_change_request.md).

The record producers capture the data that you must enter to perform the inventory allocation task. By mapping a record producer form, you can do the following tasks:

-   Pass third-party application parameters to the Telecommunications Network Inventory application. The Order Management for Telecommunications and Media \(OMT\) integration is an example. After you assign a record producer form to the change model, the assigned form appears when you select that change model. When you complete the form, the details are filled in the change request form, and the change tasks are created automatically. To learn more, see [Assign a record producer form to a change model](../task/create_record_producer_form_for_a_change_request.md).
-   Change the type of change request. The change task form includes a **Request type** field that describes the type of change request. Based on your selection, a form appears on the **Task Attributes** tab. By assigning a record producer form to the request type field of the change task, you can determine which form appears when you select a type. Based on the selected **Request type** field, a form appears under the **Task Attributes** tab. After filling out the fields in the form, the change request form updates. To learn more, see [Assign a record producer form for a request type of a change task](../task/assign_record_producer_form_for_a_change_task_of_a_change_request.md).

-   **[Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md)**  
Create, review, update, or close a change request for a change model from the network inventory workspace of the Telecommunications Network Inventory application. You can also analyze the instantiation details of the network instance.
-   **[Create and execute a change task in Telecommunications Network Inventory](../task/create-change-task-in-tni.md)**  
Create a change task after you create a change request in the Telecommunications Network Inventory application. By creating a change task, you can complete the requested change.
-   **[Revise a configuration item](revise-a-configuration-item.md)**  
Revise a CI \(Configuration Item\) of the connection to update a CI in the Telecommunications Network Inventory application.
-   **[Operationalize a configuration item](../task/operationalize-a-configuration-item.md)**  
Operationalize a Configuration Item so that you can finalize the changes and apply them on the original CI.

**Parent Topic:**[Using Telecommunications Network Inventory](using-telecom-network-inventory.md)

