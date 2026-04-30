---
title: Logical Connection Creation subflow
description: The Logical Connection enables you to create a logical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Telecommunications Network Inventory subflows, Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Logical Connection Creation subflow

The Logical Connection enables you to create a logical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.

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
|Connection elements|Connection elements that are added for the logical connections. Select the add icon \(![Add icon.](../image/add-icon-1.png)\) to add a connection element.|Array.String|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Output

The following table lists the information about the subflow's output.

|Name|Description|Data Type|
|----|-----------|---------|
|Logical Connection|Returns a glide record of the logical connection.|Reference.Logical connection|
|CI Relationship with Interface A|Returns the CI relationship with a starting network interface.|Reference.CI Relationship|
|CI Relationship with Interface Z|Returns the CI relationship with an ending network interface.|Reference.CI Relationship|

**Parent Topic:**[Telecommunications Network Inventory subflows](subflow.md)

**Related topics**  


[Physical Connection Creation subflow](physical-connection-creation-subflow.md)

[Telecommunication Network Inventory workflows in Flow Designer](telecommunication-network-inventory-workflows-flow-designer.md)

