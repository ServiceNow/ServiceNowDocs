---
title: Create CI From Template function
description: The TNI Create CI From Template function enables you to create the inventory instance in the designated site or equipment holder in the Telecommunications Network Inventory application when you instantiate an inventory with the inventory template. You can automatically create the inventory when you instantiate the network inventory design and assign process.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Function catalog, Reference, Telecommunications Network Inventory]
---

# Create CI From Template function

The TNI Create CI From Template function enables you to create the inventory instance in the designated site or equipment holder in the Telecommunications Network Inventory application when you instantiate an inventory with the inventory template. You can automatically create the inventory when you instantiate the network inventory design and assign process.

The TNI Create CI From Template function creates configuration items \(CIs\), such as the interface card, equipment, network site, and network interface, depending on the inventory template requirement.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Create CI From Template function and their description.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Network Site|sys\_id of the network site record that is associated with the new CI.|String|
|Equipment Holder|sys\_id equipment holder record that is associated with the new CI.|String|
|Inventory Template|sys\_id of the Inventory Template that is associated with the new CI.|String|
|Change Task|Change task that instantiates a new instance for the network asset.|String|
|Template Overrides|Override value if any.|String|
|Stockroom Location|Name of the stockroom location where the asset is located.|String|
|Asset|Name of the asset that is associated with this record.|String|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/action-inputs-outputs.md).

## Output

The following table lists the information about the function output.

|Name|Description|Data Type|
|----|-----------|---------|
|Record ID|Returns the sys\_id of the new inventory instance.|String|

## Example

This flow action creates a telco equipment record when you use an inventory template to instantiate equipment.

**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Cascade Update function](cascade-update-action.md)

[Create and Assign Range/Single Number function](create-assign-range-single-number-function.md)

[Create Logical Interface function](create-logical-interface-action.md)

[Create Logical Connection function](create-logical-connection-action.md)

[Create Physical Connection function](create-physical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[CIDR to IP range function](cidr_to_ip_range.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

