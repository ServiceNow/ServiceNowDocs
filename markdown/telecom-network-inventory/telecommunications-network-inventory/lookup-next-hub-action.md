---
title: Lookup Next Hub function
description: The Lookup Next Hub function enables you to take the network interface record as input and return the details of the related physical connection record. You can automatically get the details of the physical connection and interconnected ports of the equipment in the Telecommunications Network Inventory application when you use the Workflow Studio application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Lookup Next Hub function

The Lookup Next Hub function enables you to take the network interface record as input and return the details of the related physical connection record. You can automatically get the details of the physical connection and interconnected ports of the equipment in the Telecommunications Network Inventory application when you use the Workflow Studio application.

You can use the Lookup Next Hub function to return the following:

-   Physical connection that is related to the port.
-   Empty response if no physical connection is related to the port.
-   sys\_id of the front and back ports, and the port name, if there’s a configuration item \(CI\) relationship between the front and back ports.
-   NextHub interface and the interfaces that are connected to the other end of the physical connection.
-   NextHub interconnected interface and the interconnected interfaces that are connected to the other end of the physical connection.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Lookup Next Hub action and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Network Interface|Network interface record.|Reference.Network Interface|
|If multiple records are found action|Option to select the action when multiple records are found. You can select **Return only the first record** from the list to return the details of the first physical connection record.|Choice|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Output

The following table lists the information about the function output.

|Name|Description|Data Type|
|----|-----------|---------|
|Physical Connections|Returns the list of sys\_ids of the physical connection records that are related to the network interface.|Array.String|
|Interconnected Port|Returns the list of sys\_ids of the ports that are interconnected to the network interface.|Array.String|
|NextHub Interface|Returns the list of sys\_ids of the interfaces that are connected to the other end of the physical connection.|Array.String|
|NextHub Interconnected Interface|Returns the list of sys\_ids of the interconnected interfaces that are connected to the other end of the physical connection.|Array.String|

## Example

-   **Use Case 1**

    If the input is passed as Interface-1 of Equipment-1 as shown in the following example, the function returns empty records, because the network inventory has no physical or internal connections in the network inventory.

    ![Display of use case 1 where Interface-1 is connected to Equipment-1.](../image/cascade-action-1.png)

-   **Use Case 2**

    If the input is passed as Interface-1 of Equipment-1 as shown in the following example, the function returns the network interface record of Interface-2.

    ![Display of use case 2 where Interface-2 and Interface-1 are connected to Equipment-1.](../image/cascade-action-2.png)

-   **Use Case 3**

    If the input is passed as Interface-1 of Equipment-1 as shown in the following example, the function returns the network interface record of Interface-2 and the physical connection record of PC-1.

    ![Display of use case 3 where Interface-2 and Interface-1 are connected to Equipment-1, and Interface-3 is connected to Equipment-2, and there is a physical connection between Interface 1 and 3.](../image/cascade-action-3.png)

-   **Use Case 4**

    If the input is passed as Interface-1 of Equipment-1 as shown in the following example, the NextHub Interface is 3 and the NextHub Interconnected Interface is 4.

    ![Display of use case 4 where Interface-2 and Interface-1 are connected to Equipment-1, Interface-3 and Interface-4 are connected to Equipment-2, and there is a physical connection between Interface-1 and Interface-3.](../image/cascade-action-4.png)


**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Create CI From Template function](add-card-action.md)

[Cascade Update function](cascade-update-action.md)

[Create and Assign Range/Single Number function](create-assign-range-single-number-function.md)

[Create Logical Interface function](create-logical-interface-action.md)

[Create Logical Connection function](create-logical-connection-action.md)

[Create Physical Connection function](create-physical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[CIDR to IP range function](cidr_to_ip_range.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Path Search function](path-compute-action.md)

