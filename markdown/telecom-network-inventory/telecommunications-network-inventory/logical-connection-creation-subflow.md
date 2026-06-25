---
title: Logical Connection Creation subflow
description: The Logical Connection Creation subflow enables you to create a logical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/logical-connection-creation-subflow.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Subflows, Reference, Telecommunications Network Inventory]
---

# Logical Connection Creation subflow

The Logical Connection Creation subflow enables you to create a logical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.

You can use the Logical Connection subflow to create a logical connection on your network interface cards.

This subflow also creates the connection elements and associates them to the logical connection.

If you enter a network interface, equipment, physical connection, logical connection, or managed function as a connection element, the Logical Connection Creation subflow creates the corresponding connection element.

## Roles and availability

Users with the admin role can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Logical Connection Creation subflow and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Interface A|Starting network interface where this logical connection is configured.|Reference.Network Interface|
|Interface Z|Ending network interface where this logical connection is configured.|Reference.Network Interface|
|Bandwidth|Bandwidth of the logical connection.|Reference.Bandwidth|
|Connection Type|Type of connection. This field information updates the product model that is associated with the physical connection.|Reference.Logical Connection Model|
|Connection elements|Connection elements that are added for the logical connections. Select the add icon \(\[Omitted image "add-icon-1.png"\] Alt text: Add icon.\) to add a connection element.|Array.String|

To learn more about the variable data types, see Flow Designer input and output data variables.

## Output

The following table lists the information about the subflow's output.

|Name|Description|Data Type|
|----|-----------|---------|
|Logical Connection|Returns a glide record of the logical connection.|Reference.Logical connection|
|CI Relationship with Interface A|Returns the CI relationship with a starting network interface.|Reference.CI Relationship|
|CI Relationship with Interface Z|Returns the CI relationship with an ending network interface.|Reference.CI Relationship|

**Parent Topic:**[Telecommunications Network Inventory subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/subflow.md)

**Related topics**  


[Create Logical Connection with template subflow]()

[Physical connection creation subflow]()

[Design Assign Connection Element Creation subflow]()

[Design Assign Protected Path Assignment subflow]()

[Design Assign IP Address Creation subflow]()

[Design assign Logical Connection Creation subflow]()

[Design Assign Number Element Creation subflow]()

[Design Assign Set Attributes subflow]()

[Design Assign Request Details Update subflow]()

[Design Assign Connection Element Validation subflow]()

[Design Assign IP Address Validation subflow]()

[Design Assign Number Element Validation subflow]()

[Workflows in Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunication-network-inventory-workflows-flow-designer.md)

