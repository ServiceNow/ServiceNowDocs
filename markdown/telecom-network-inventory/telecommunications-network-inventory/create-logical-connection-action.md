---
title: Create Logical Connection function
description: The Create Logical Connection function enables you to create a logical connection record in the Telecommunications Network Inventory application based on the input \(interfaces\) that you receive when you instantiate an inventory.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Create Logical Connection function

The Create Logical Connection function enables you to create a logical connection record in the Telecommunications Network Inventory application based on the input \(interfaces\) that you receive when you instantiate an inventory.

You can use the Create Logical Connection function to create a logical connection on your network interface cards.

When you enter the Interface A, this function automatically retrieves the data for Site A, Equipment A, and Port A. Similarly, after passing input Interface Z, the function retrieves the data for the associated Site Z, Equipment Z, and Port Z. This function also retrieves the data for Bandwidth AtoZ and Bandwidth ZtoA from the Bandwidth field.

This function also creates the connection elements and associates them to the logical connection.

If you configure a network interface, equipment, physical connection, logical connection, or managed function as a connection element, the Logical Connection Creation function creates the corresponding connection element and associates it to a logical connection.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Create Logical Connection function and their descriptions.

<table id="table_w3g_2fm_1vb"><thead><tr><th>

Field Name

</th><th>

Description

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Interface A

</td><td>

Starting network interface where this logical connection is configured.

</td><td>

Reference.Network Interface

</td></tr><tr><td>

Interface Z

</td><td>

Ending network interface where this logical connection is configured.

</td><td>

Reference.Network Interface

</td></tr><tr><td>

Bandwidth

</td><td>

Bandwidth of the logical connection.

</td><td>

Reference.Bandwidth

</td></tr><tr><td>

Connection Type

</td><td>

Type of connection. This field information updates the product model that is associated with the physical connection.

</td><td>

Reference.Logical Connection Model

</td></tr><tr><td>

Connection elements

</td><td>

Connection elements that are added for the logical connections. Click the add icon \(![Add icon.](../image/add-icon-1.png)\) to add a connection element.

</td><td>

Array.String

</td></tr></tbody>
</table>To learn more about the variable data types, see Flow Designer input and output data variables.

## Output

The following table lists the information about the function output.

|Name|Description|Data Type|
|----|-----------|---------|
|Logical Connection|Returns a glide record of the logical connection.|Record|

**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Create CI From Template function](add-card-action.md)

[Cascade Update function](cascade-update-action.md)

[Create and Assign Range/Single Number function](create-assign-range-single-number-function.md)

[Create Logical Interface function](create-logical-interface-action.md)

[Create Physical Connection function](create-physical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[CIDR to IP range function](cidr_to_ip_range.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

