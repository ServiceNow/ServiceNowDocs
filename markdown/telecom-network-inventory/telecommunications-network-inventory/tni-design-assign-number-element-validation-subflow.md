---
title: TNI Design Assign Number Element Validation subflow
description: The TNI Design Assign Number Element Validation subflow enables you to validate the number element records in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Telecommunications Network Inventory subflows, Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# TNI Design Assign Number Element Validation subflow

The TNI Design Assign Number Element Validation subflow enables you to validate the number element records in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.

The TNI Design Assign Number Element Validation subflow validates whether the number element records required for the Define number element activity have already been used or not. If the number elements are already used, the subflow passes the information.

## Roles and availability

An admin can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the TNI Design Assign Number Element Validation subflow and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Change Task|The change task that is associated with Define number element activity.|Reference.Change Task|
|Ignore Validation Error|Ignores any validation errors.|True/False|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Output

If the number element is already used, then the subflow passes the following message "**Number element has already been created. Please try creating another one.**"

**Parent Topic:**[Telecommunications Network Inventory subflows](subflow.md)

**Related topics**  


[Create Logical Connection with template subflow](create-logical-connection-template-subflow.md)

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

