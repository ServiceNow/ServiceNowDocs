---
title: Create Physical Connection function
description: The Create Physical Connection function enables you to create a physical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Create Physical Connection function

The Create Physical Connection function enables you to create a physical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.

You can use the Create Physical Connection function to create a physical port connection on the interface cards in your networks.

When you enter the Interface A, this function automatically retrieves the data for related Site A, Equipment A, and Port A. Similarly, after passing input Interface Z, the function retrieves the data for associated Site Z, Equipment Z, and Port Z. This function also retrieves the data for Bandwidth AtoZ and Bandwidth ZtoA from the Bandwidth field.

This function also creates the connection elements and associates them to the physical connection.

If you pass a physical connection element, this subflow creates the corresponding connection element and associates it to the physical connection.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Create Physical Connection function and their description.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Interface A|Starting network interface where this logical connection is configured.|Reference.Network Interface|
|Interface Z|Ending network interface where this logical connection is configured.|Reference.Network Interface|
|Bandwidth|Bandwidth of the logical connection.|Reference.Bandwidth|
|Connection Type|Type of connection. This field information updates the Product Model that is associated with the physical connection.|Reference.Physical Connection Model|
|Physical Connection Elements|sys\_id of the connection elements that are added for the physical connections. If the physical connection has the Connection Type attribute as Cable, you can add the connection element. Click the add icon \(![Add icon.](../image/add-icon-1.png)\) to add a connection element.|Array.String|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/action-inputs-outputs.md).

## Output

The following table lists the information about the function output.

|Name|Description|Data Type|
|----|-----------|---------|
|Physical Connection|Returns a glide record of the physical connection.|Record|

**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Create CI From Template function](add-card-action.md)

[Cascade Update function](cascade-update-action.md)

[Create and Assign Range/Single Number function](create-assign-range-single-number-function.md)

[Create Logical Interface function](create-logical-interface-action.md)

[Create Logical Connection function](create-logical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[CIDR to IP range function](cidr_to_ip_range.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

