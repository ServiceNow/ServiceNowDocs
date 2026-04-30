---
title: Instantiating your network inventory by using design and assign
description: By instantiating your network inventory in the Telecommunications Network Inventory application, you can generate and validate your inventory records at the site level. You can also generate your individual network instances from your defined inventory templates and models and then verify that they’re properly configured.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
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
-   **[Create a Link Aggregation Group using design and assign function](../task/create_a_change_request_by_using_the_design_assign_link_aggregation_group.md)**  
Design and assign a Link Aggregation Group \(LAG\) with the creation of Ethernet connections in the Telecommunications Network Inventory application. By creating a LAG connection, you can fulfill an order request from the customer.
-   **[Add or remove a member to Link Aggregation](../task/create-a-change-request-to-add-or-remove-member-to-link-aggregation.md)**  
Create a change request to add or remove a member to the design assign link aggregation change request by using the Telecommunications Network Inventory application.
-   **[Design your GPON Broadband Service](../task/gpon-broadband-change-model.md)**  
Design and assign your Gigabyte Passive Optical Network \(GPON\) broadband service in the Telecommunications Network Inventory application. The GPON Broadband Service change model enables you to create multiple change tasks so that you can fulfill an order request for a GPON broadband service.
-   **[Modify logical connection endpoints model](../task/create-a-change-request-by-using-modify-logical-connection-endpoints-model.md)**  
Modify logical connection endpoints and its details using design and assign function in the Telecommunications Network Inventory application. By making changes in the logical connection endpoints, you can fulfill an order request from the customer.
-   **[Modify physical connection endpoints](../task/create-a-change-request-by-using-modify-physical-connection.md)**  
Modify physical connection endpoints and it's details using design and assign function in the Telecommunications Network Inventory application. By making changes in the physical connection endpoints, you can fulfill an order request from the customer.
-   **[Create a network topology record by using design and assign](../task/instantiate-network-topology-design-assign.md)**  
Create a network topology record using the design and assign function in the Telecommunications Network Inventory application. By creating the network topology, you can visualize how the network elements are organized and connected to one another.
-   **[Add or remove a member to network topology record](../task/modify-network-topology-record-design-assign.md)**  
Modify a network topology record using the design and assign function in the Telecommunications Network Inventory application. You can add or delete the elements in an existing network topology record and visualize how the network elements are organized and connected to one another.
-   **[Create a cable record by using design and assign](../task/create-cable-record-using-design-assign.md)**  
Create a cable record using the design and assign function in the Telecommunications Network Inventory application. By creating the cable and related strand records, you can fulfill an order request for a fiber optical cable record.
-   **[Create an equipment record by using design and assign](../task/create-equipment-record-design-and-assign.md)**  
Create an equipment record using the design and assign function in the Telecommunications Network Inventory application. By creating the equipment and its related inventory records, you can fulfill an order request for an equipment record.
-   **[Create and execute a change task in Telecommunications Network Inventory](../task/create-change-task-in-tni.md)**  
Create a change task after you create a change request in the Telecommunications Network Inventory application. By creating a change task, you can complete the requested change.
-   **[Add a card to equipment](../task/add-card-equipment-design-assign-function.md)**  
Add a card to equipment record using design and assign function in the Telecommunications Network Inventory application. By adding a card, you can fulfill an order request for a customer requirement.
-   **[Add an equipment or rack to logical composite](../task/add-equipment-rack-logical-composite.md)**  
Add equipment or rack to a logical composite using design and assign.
-   **[Remove an equipment or rack from logical composite](../task/remove-equipment-rack-logical-composite.md)**  
Remove a rack or equipment from a logical composite using design and assign.
-   **[Add an equipment to rack or cabinet](../task/add-equipment-rack.md)**  
Add equipment to a rack or cabinet using design and assign function in the Telecommunications Network Inventory application. By adding the equipment to rack, you can fulfill a customer order request.
-   **[Remove an equipment or shelf from a rack or cabinet](../task/remove-equipment-shelf-rack-cabinet.md)**  
Remove an equipment or shelf from a rack or cabinet using design and assign function in the Telecommunications Network Inventory application. By removing the equipment from rack, you can fulfill a customer order request.
-   **[Create logical connection record using design and assign](../task/create-logical-connection-record-using-design-assign.md)**  
Create a logical connection record using the design and assign function in the Telecommunications Network Inventory application. By creating the logical connection and its related inventory records, you can fulfill an order request for an equipment record.
-   **[Create physical connection using design and assign](../task/create-physical-connection-design-assign.md)**  
Create an physical connection record using the design and assign function in the Telecommunications Network Inventory application. By creating the physical connection and its related inventory records, you can fulfill an order request for an equipment record.
-   **[Revise a configuration item using design and assign](revise-a-configuration-item.md)**  
Revise a CI \(Configuration Item\) of the connection to update a CI in the Telecommunications Network Inventory application.
-   **[Operationalize a configuration item](../task/operationalize-a-configuration-item.md)**  
Operationalize a Configuration Item so that you can finalize the changes and apply them on the original CI.

**Parent Topic:**[Using Telecommunications Network Inventory](using-telecom-network-inventory.md)

