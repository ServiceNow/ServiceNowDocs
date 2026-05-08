---
title: Create Logical Interface function
description: The Create Logical Interface function enables you to create logical interfaces in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Create Logical Interface function

The Create Logical Interface function enables you to create logical interfaces in the Telecommunications Network Inventory application.

You can use the Create Logical Interface function to create the logical interfaces that are created either as a termination point for logical connections or as a child of a physical or logical interface. A physical or logical Interface can have multiple child logical interfaces. The bandwidth of the logical Interface isn’t fixed and you can configure it as applicable. Also, this function sets the virtual flag of the logical network interface.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Create Logical Interface function and their descriptions.

<table id="table_w3g_2fm_1vb"><thead><tr><th>

Field Name

</th><th>

Description

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Parent Interface

</td><td>

Parent network interface record to create the relationship with a logical interface. Click the add icon \(![Add icon](../image/add-icon-1.png)\) to add an interface.

</td><td>

Array.String

</td></tr><tr><td>

Name

</td><td>

Name of the new logical interface.**Note:** If you don’t enter the logical interface name, this flow action generates the model name with the number after the maximum number of unit positions.

</td><td>

String

</td></tr><tr><td>

Type

</td><td>

Optional user-defined type code that you use to categorize the types of various network entities or assets.

</td><td>

Reference.TRF Value

</td></tr><tr><td>

Role

</td><td>

Optional user-defined role code that you use to categorize the roles or purposes of the various network entities or assets.

</td><td>

Reference.TRF Value

</td></tr><tr><td>

Function

</td><td>

Optional user-defined function code that you use to categorize the functions of the various network entities or assets.

</td><td>

Reference.TRF Value

</td></tr><tr><td>

Telco Equipment

</td><td>

Equipment that is associated with the logical interface. If you do not enter the name of the equipment, this function selects the associated equipment from the parent interface.

</td><td>

Reference.Telco equipment

</td></tr><tr><td>

Port Bandwidth

</td><td>

Bandwidth of this logical connection.

</td><td>

Reference.Bandwidth

</td></tr><tr><td>

Product Model

</td><td>

Network interface model that is associated with the logical interface.

</td><td>

Reference.Network Interface Model

</td></tr><tr><td>

CI Relationship

</td><td>

Type of CI relationship. By default, the Create Logical Interface flow action sets the CI relationship to **Contains : Contained By**. The parent interface can support multiple interface record references as an input. If you enter the same parent CI more than once, the system ensures that it associates to a unique set of parent-child relationship.

</td><td>

Reference.CI Relationship

</td></tr><tr><td>

Aggregation Interface

</td><td>

Option to ensure that each parent interface must only have one child interface.

</td><td>

True/False

</td></tr></tbody>
</table>To learn more about the variable data types, see Flow Designer input and output data variables.

## Output

The following table lists the information about the function output.

|Name|Description|Data Type|
|----|-----------|---------|
|Result Id|Returns a glide record of the logical interface.|Record|

**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Create CI From Template function](add-card-action.md)

[Cascade Update function](cascade-update-action.md)

[Create and Assign Range/Single Number function](create-assign-range-single-number-function.md)

[Create Logical Connection function](create-logical-connection-action.md)

[Create Physical Connection function](create-physical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[CIDR to IP range function](cidr_to_ip_range.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

