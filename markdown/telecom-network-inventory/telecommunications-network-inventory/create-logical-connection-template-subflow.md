---
title: Create Logical Connection with template subflow
description: The Create Logical Connection with template subflow enables you to create a logical connection record from an inventory template in the Telecommunications Network Inventory application. The logical connection record is created based on the input that you receive when you instantiate an inventory using an inventory template.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Telecommunications Network Inventory subflows, Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Create Logical Connection with template subflow

The Create Logical Connection with template subflow enables you to create a logical connection record from an inventory template in the Telecommunications Network Inventory application. The logical connection record is created based on the input that you receive when you instantiate an inventory using an inventory template.

You can use the Create Logical Connection with template subflow to create a logical connection from an inventory template on your network interface cards.

This subflow also creates the connection elements and associates them to the logical connection.

If you enter a network interface, equipment, physical connection, logical connection, or managed function as a connection element, the Logical Connection Creation subflow creates the corresponding connection element.

## Roles and availability

Users with the admin role can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Create Logical Connection with template subflow and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Interface A|Starting network interface where this logical connection is configured.|Reference.Network Interface|
|Interface Z|Ending network interface where this logical connection is configured.|Reference.Network Interface|
|Change Task|Change task to instantiate a logical connection using a template.|Reference.Change Task|
|Interface A|Starting network interface where this logical connection is configured.|Reference.Network interface|
|Interface Z|Ending network interface where this logical connection is configured.|Reference.Network interface|
|Bandwidth A|Bandwidth at the starting logical connection.|Reference.Bandwidth|
|Bandwidth Z|Bandwidth at the ending logical connection.|Reference.Bandwidth|
|Connection Type|Type of connection. This field information updates the product model that is associated with the physical connection.|Reference.Logical Connection Model|
|Logical Connection Template|Template associated with logical connection.|Reference.Inventory Template|
|Connection elements|Connection elements that are added for the logical connections. Select the add icon \(![Add icon.](../image/add-icon-1.png)\) to add a connection element.|Array.String|
|Position|Unit position of this logical connection.|Integer|
|A End Interface Name|Starting interface name.|String|
|Z End Interface Name|Ending interface name.|String|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Output

The following table lists the information about the subflow's output.

|Name|Description|Data Type|
|----|-----------|---------|
|Logical Connection|Returns a glide record of the logical connection.|Reference.Logical connection|
|CI Relationship with Interface A|Returns the CI relationship with a starting network interface.|Reference.CI Relationship|
|CI Relationship with Interface Z|Returns the CI relationship with an ending network interface.|Reference.CI Relationship|

**Parent Topic:**[Telecommunications Network Inventory subflows](subflow.md)

**Related topics**  


[Logical Connection Creation subflow](logical-connection-creation-subflow.md)

[Physical Connection Creation subflow](physical-connection-creation-subflow.md)

[TNI Design Assign Connection Element Creation subflow](tni-design-assign-connection-element-creation-subflow.md)

[TNI Design Assign Protected Path Assignment subflow](tni-design-assign-protected-path-assignment-subflow.md)

[TNI Design Assign IP Address Creation subflow](tni-design-assign-ip-address-creation-subflow.md)

[TNI Design assign Logical Connection Creation subflow](tni-design-assign-logical-connection-creation-subflow.md)

[TNI Design Assign Number Element Creation subflow](tni-design-assign-number-element-creation-subflow.md)

[TNI Design Assign Set Attributes subflow](tni-design-assign-set-attributes-subflow.md)

[TNI Design Assign Request Details Update subflow](tni-design-assign-request-details-update-subflow.md)

[TNI Design Assign Connection Element Validation subflow](tni-design-assign-connection-element-validation-subflow.md)

[TNI Design Assign IP Address Validation subflow](tni-design-assign-ip-address-validation-subflow.md)

[TNI Design Assign Number Element Validation subflow](tni-design-assign-number-element-validation-subflow.md)

