---
title: Allocate Free Number function
description: The Allocate Free Number function enables you to assign free numbers from the Telecommunications Network Inventory number record. You use this function to allocate a quantity of numbers from a specified range to add against the configuration item \(CI\) in a number element.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/allocate-free-number-action.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Allocate Free Number function

The Allocate Free Number function enables you to assign free numbers from the Telecommunications Network Inventory number record. You use this function to allocate a quantity of numbers from a specified range to add against the configuration item \(CI\) in a number element.

You use the Allocate Free Number function to do the following actions:

-   Assign the free number from a number range that is in the inventory record.
-   Get the free number from the number range and create the inventory number record as a child number.
-   Add the free numbers against the CI in a number element.

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

</th></tr></thead><tbody><tr><td>

Number Range

</td><td>

Inventory number record where you need the free number for.

</td><td>

Reference.Inventory Number record

</td></tr><tr><td>

Count

</td><td>

Total count of the free numbers.

</td><td>

Integer

</td></tr><tr><td>

Number Type

</td><td>

Type of network connection that you need the free numbers for. Select one of the following:-   **VLAN**

Single VLAN number record.

-   **LAG**

Single LAG number record.


</td><td>

Choice

</td></tr><tr><td>

Owned by configuration item

</td><td>

Configuration item \(CI\) that is related to the Inventory number record.

</td><td>

Reference.Configuration Item

</td></tr><tr><td>

Consecutive

</td><td>

Option to return the consecutive free numbers.

</td><td>

True/False

</td></tr></tbody>
</table>To learn more about the variable data types, see Flow Designer input and output data variables.

## Output

The following table lists the information about the function output.

|Name|Description|Type|
|----|-----------|----|
|FinalRecordList|Returns the list of inventory number records for the number range.|Array.Integer|

## Example

Consider that a VLAN has 1–4096 as the number range and 1–1000, 1001–2500, and 2510–4096 are the subranges. If you give the count as 4, the function returns the list of inventory number records for 2501, 2502, 2503, and 2504. These numbers are free in the VLAN number range.

**Parent Topic:**[Telecommunications Network Inventory function catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-flow-action.md)

**Related topics**  


[Create CI From Template function]()

[Cascade Update function]()

[Create and Assign Range/Single Number function]()

[Create Logical Interface function]()

[Create Logical Connection function]()

[Create Physical Connection function]()

[Create IP subnetwork function]()

[CIDR to IP range function]()

[Get Interface Summary function]()

[Lookup Next Hub function]()

[Path Search function]()

