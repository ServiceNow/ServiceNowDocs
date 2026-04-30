---
title: Path Search function
description: The Path Search function enables you to execute the path computation function between the starting and ending sites in the Telecommunications Network Inventory application. You can use this function for the path computation when you process the network inventory design and assign.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Telecommunications Network Inventory function catalog, Reference, Telecommunications Network Inventory]
---

# Path Search function

The Path Search function enables you to execute the path computation function between the starting and ending sites in the Telecommunications Network Inventory application. You can use this function for the path computation when you process the network inventory design and assign.

You can use the Path Search function to identify the possible paths between your network sites.

If no path is found, the Path Search function uses the available input to create a logical connection without adding any connection elements. If you don’t enter the end equipment, it selects any equipment that matches the Type attribute that belongs to the end site. The function uses the start and end interfaces in the input to set the Port A and Port Z of the logical connections. Otherwise, it selects any interface in the Availability field, which is marked as Available.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Path Search function and their description.

<table id="table_w3g_2fm_1vb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Start Site

</td><td>

sys\_id of the starting network site where this connection is configured.

</td><td>

String

</td></tr><tr><td>

End Site

</td><td>

sys\_id of the ending network site where this connection is configured.

</td><td>

String

</td></tr><tr><td>

Start Equipment

</td><td>

sys\_id of the starting network equipment where this connection is configured.

</td><td>

String

</td></tr><tr><td>

End Equipment

</td><td>

sys\_id of the ending network equipment where this connection is configured.

</td><td>

String

</td></tr><tr><td>

Start Interface

</td><td>

sys\_id of the starting network interface where this connection is configured.**Note:** If this field is left empty, it automatically selects the interface by using the path computation to create a logical connection.

</td><td>

String

</td></tr><tr><td>

End Interface

</td><td>

sys\_id of the ending network interface where this connection is configured.**Note:** If this field is left empty, it automatically selects the interface by using the path computation to create a logical connection.

</td><td>

String

</td></tr><tr><td>

End Equipment Type

</td><td>

sys\_id of the ending network equipment type where this connection is configured.

</td><td>

String

</td></tr><tr><td>

Logical Connection Model

</td><td>

sys\_id of the logical connection model where this connection is configured.

</td><td>

String

</td></tr><tr><td>

Bandwidth

</td><td>

sys\_id of the bandwidth of the connection.

</td><td>

String

</td></tr><tr><td>

Allowed Logical Connection Model

</td><td>

sys\_id of the supported models for the logical connection. Click the add icon \(![Add icon.](../image/add-icon-1.png)\) to add a logical connection model.

</td><td>

Array.String

</td></tr><tr><td>

Allowed Physical Connection Model

</td><td>

sys\_id of the supported models for the physical connection. Click the add icon \(![Add icon.](../image/add-icon-1.png)\) to add a physical connection model.

</td><td>

Array.String

</td></tr><tr><td>

Fail Action

</td><td>

Option to select the action when the function fails. You can select an action from the list. By default, the **Create logical connection without path elements** is selected.

</td><td>

Choice

</td></tr></tbody>
</table>To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Output

The following table lists the information about the function's output.

|Name|Description|Data Type|
|----|-----------|---------|
|Connection id|Returns the sys\_id of the logical connection record.|String|

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

[Lookup Next Hub function](lookup-next-hub-action.md)

