---
title: Get Interface Summary function
description: The Get Interface Summary function enables you to retrieve all the network interface records that are associated with the input. You can use this function to automatically get the details of the available interface, connected interface, and the physical connection of the equipment in the Telecommunications Network Inventory application when you use Workflow Studio.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Get Interface Summary function

The Get Interface Summary function enables you to retrieve all the network interface records that are associated with the input. You can use this function to automatically get the details of the available interface, connected interface, and the physical connection of the equipment in the Telecommunications Network Inventory application when you use Workflow Studio.

The Get Interface Summary function enables you to retrieve the network interface records that are associated with the input such as Site, Rack, or Equipment. You must enter the site, equipment, or rack value to return the output.

If multiple inputs don't match, the action reports an error. For example, let's say that you can see the equipment and site details but because the equipment doesn’t belong to the site, the system reports an error with the conflict information.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Get Interface Summary function and their descriptions.

<table id="table_w3g_2fm_1vb"><thead><tr><th>

Field Name

</th><th>

Description

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Site

</td><td>

Network site that is associated with the network interface.

</td><td>

Reference.Network Site

</td></tr><tr><td>

Rack

</td><td>

Rack that is associated with the network interface.

</td><td>

Reference.Telco equipment

</td></tr><tr><td>

Equipment

</td><td>

Equipment that is associated with the network interface.

</td><td>

Reference.Telco equipment

</td></tr><tr><td>

Availability

</td><td>

Status of the network asset. You can select one from the following options:

-   Available
-   Used
-   Reserved
-   Shared

</td><td>

Choice

</td></tr><tr><td>

Model

</td><td>

Physical connection model that is associated with the network interface.

</td><td>

Reference.Physical Connection Model

</td></tr><tr><td>

Type

</td><td>

Optional user-defined type code that you use to categorize the types of the various network entities or assets.

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

If multiple records are found action

</td><td>

Option to return the type of output when multiple records are found. You can select **Return only the first record** from the list to return the first interface network record.

</td><td>

Choice

</td></tr></tbody>
</table>To learn more about the variable data types, see [Flow Designer input and output data variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/action-inputs-outputs.md).

## Output

The following table lists the information about the function output.

|Name|Description|Data Type|
|----|-----------|---------|
|Available Interfaces|Returns the sys\_id list of the available network interfaces.|Array.String|
|Connected Interfaces|Returns the sys\_id list of the network interfaces that are connected to the other network assets.|Array.String|
|Physical Connections|Returns the sys\_id list of the physical connections.|Array.String|

## Example

If the input is passed as Equipment-1 as shown in the following example where Port-1, Port-2, and Port-3 are connected to Equipment-1, Port-4 and Port-5 are connected to Equipment-2, physical connection-1 between Port-2 and Port-4, and physical connection-2 between Port-3 and Port-5. Then the output is as follows:

-   Available Interface - Port-1
-   Connected Interfaces - Port-2 and Port-3
-   physical Connections - PC-1 and PC-2

![Infographic displaying the connections from the Get Interface Summary action. For the text description, refer to the example description that follows.](../image/get-interface-summary-example.png)

If you select **If multiple records are found action** as **Return only the first record**, it returns Port-1, Port-2, and PC-1, respectively.

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

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

