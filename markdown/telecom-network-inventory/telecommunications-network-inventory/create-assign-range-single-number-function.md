---
title: Create and Assign Range/Single Number function
description: The Create and Assign Range/Single Number function enables you to create the inventory number records for a number range when you process the network inventory workflow.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Telecommunications Network Inventory function catalog, Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Create and Assign Range/Single Number function

The Create and Assign Range/Single Number function enables you to create the inventory number records for a number range when you process the network inventory workflow.

You use the Create and Assign Range/Single Number function to create the inventory number records between the input start and end numbers. This function also creates the corresponding number elements.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

An admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Allocate Free Number action and their descriptions.

<table id="table_w3g_2fm_1vb"><thead><tr><th>

Field Name

</th><th>

Description

</th><th>

Type

</th><th>

Required?

</th></tr></thead><tbody><tr><td>

Owned By Configuration Item

</td><td>

Inventory number record that you need the free number for.

</td><td>

Reference.Configuration Item

</td><td>

Yes

</td></tr><tr><td>

Start

</td><td>

Start number of the inventory number record.

</td><td>

Integer

</td><td>

Yes

</td></tr><tr><td>

End

</td><td>

End number of the inventory number record. You must provide the value when it’s a range.

</td><td>

Integer

</td><td>

No

</td></tr><tr><td>

Name

</td><td>

Name of the inventory number record that you want to create.

</td><td>

String

</td><td>

Yes

</td></tr><tr><td>

Number Type

</td><td>

Type of network connection that you need the free numbers for. Select one of the following:-   **VLAN Range**

Range of VLAN numbers.

-   **VLAN Subrange**

Subset or a range of VLAN numbers within the overall VLAN range.

-   **VLAN**

Single VLAN number record

-   **LAG Range**

Range of LAG numbers.

-   **LAG**

Single LAG number record


</td><td>

Choice

</td><td>

Yes

</td></tr><tr><td>

Parent Number

</td><td>

Parent number record. If you don't select the parent number record, the function returns only an inventory number record for the start number.

</td><td>

Reference.Inventory Number record

</td><td>

No

</td></tr></tbody>
</table>To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Output

The following table lists the information about the function output.

|Name|Description|Type|
|----|-----------|----|
|Inventory Number|Returns the inventory number record.|Record|

## Example

Consider, a VLAN has 1–4096 as range and 1–1000, 1001–2500, and 2510–4096 are the subranges. If you give the start number as 2501 and the end number as 2502, the function creates a number range of 2501-2502 and returns the inventory number record.

**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Create CI From Template function](add-card-action.md)

[Cascade Update function](cascade-update-action.md)

[Create Logical Interface function](create-logical-interface-action.md)

[Create Logical Connection function](create-logical-connection-action.md)

[Create Physical Connection function](create-physical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[CIDR to IP range function](cidr_to_ip_range.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

