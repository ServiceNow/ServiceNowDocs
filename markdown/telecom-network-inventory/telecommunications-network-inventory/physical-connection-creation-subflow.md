---
title: Physical Connection Creation subflow
description: The Physical Connection Creation subflow enables you to create a physical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Subflows, Reference, Telecommunications Network Inventory]
---

# Physical Connection Creation subflow

The Physical Connection Creation subflow enables you to create a physical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory.

You can use the Physical Connection Creation subflow to create a physical port connection on the interface cards in your networks.

This subflow also creates the connection elements and associates them to the physical connection.

If you enter a physical connection element, this subflow creates the corresponding connection element and associates it to the physical connection.

## Roles and availability

Users with the admin role can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Physical Connection Creation subflow and their description.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Interface A|Starting network interface where this logical connection is configured.|Reference.Network Interface|
|Interface Z|Ending network interface where this logical connection is configured.|Reference.Network Interface|
|Bandwidth|Bandwidth of the logical connection.|Reference.Bandwidth|
|Connection Type|Type of connection. This field information updates the product model that is associated with the physical connection.|Reference.Physical Connection Model|
|CI Relationship|Type of configuration item \(CI\) relationship. By default, the Logical Creation subflow sets a CI relationship to **Terminated::Terminated by**.|Reference.CI Relationship Type|
|Physical connection elements|sys\_id of the connection elements that are added for the physical connections. If the physical connection has the Connection Type attribute as Cable, you can add the connection element. Click the add icon \(![Add icon.](../image/add-icon-1.png)\) to add a connection element.|Array.String|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Output

The following table lists the information about the subflow's output.

|Name|Description|Data Type|
|----|-----------|---------|
|Physical Connection|Returns a glide record of the physical connection.|Record|
|CI Relationship with Interface Z|Returns the CI relationship with an ending network interface.|Reference.CI Relationship|
|CI Relationship with Interface A|Returns the CI relationship with a starting network interface.|Reference.CI Relationship|

**Parent Topic:**[Telecommunications Network Inventory subflows](subflow.md)

**Related topics**  


[Create Logical Connection with template subflow](create-logical-connection-template-subflow.md)

[Logical Connection Creation subflow](logical-connection-creation-subflow.md)

[Design Assign Connection Element Creation subflow](tni-design-assign-connection-element-creation-subflow.md)

[Design Assign Protected Path Assignment subflow](tni-design-assign-protected-path-assignment-subflow.md)

[Design Assign IP Address Creation subflow](tni-design-assign-ip-address-creation-subflow.md)

[Design assign Logical Connection Creation subflow](tni-design-assign-logical-connection-creation-subflow.md)

[Design Assign Number Element Creation subflow](tni-design-assign-number-element-creation-subflow.md)

[Design Assign Set Attributes subflow](tni-design-assign-set-attributes-subflow.md)

[Design Assign Request Details Update subflow](tni-design-assign-request-details-update-subflow.md)

[Design Assign Connection Element Validation subflow](tni-design-assign-connection-element-validation-subflow.md)

[Design Assign IP Address Validation subflow](tni-design-assign-ip-address-validation-subflow.md)

[Design Assign Number Element Validation subflow](tni-design-assign-number-element-validation-subflow.md)

[Workflows in Flow Designer](telecommunication-network-inventory-workflows-flow-designer.md)

