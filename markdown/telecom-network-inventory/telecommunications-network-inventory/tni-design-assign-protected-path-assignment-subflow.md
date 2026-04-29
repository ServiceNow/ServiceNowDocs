---
title: Design Assign Protected Path Assignment subflow
description: The TNI Design Assign Connection Element Creation subflow enables you to update the protection path in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Subflows, Reference, Telecommunications Network Inventory]
---

# Design Assign Protected Path Assignment subflow

The TNI Design Assign Connection Element Creation subflow enables you to update the protection path in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.

The TNI Design Assign Protected Path Assignment subflow gets the protection paths that are associated with a logical connection and updates them in a change task. This subflow functions are as follows.

-   Get the details from the Assign protection element activity.
-   Update the protection path in the logical connection record.
-   Create CI relationship between logical connection and protected path.
-   Update change task that is associated with the Assign protection element activity.

## Roles and availability

An admin can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the TNI Design Assign Protected Path Assignment subflow and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Change Task|The change task that is associated with Assign protection element activity.|Reference.Change Task|
|Ignore Validation Error|Ignores any validation errors.|True/False|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Output

The TNI Design Assign Protected Path Assignment subflow output are as follows.

-   Update the protection path in the logical connection.
-   Create the CI relationship between logical connection and protection path.
-   Update change task that is associated with the Assign protection element activity.

**Parent Topic:**[Telecommunications Network Inventory subflows](subflow.md)

**Related topics**  


[Create Logical Connection with template subflow](create-logical-connection-template-subflow.md)

[Logical Connection Creation subflow](logical-connection-creation-subflow.md)

[Physical Connection Creation subflow](physical-connection-creation-subflow.md)

[Design Assign Connection Element Creation subflow](tni-design-assign-connection-element-creation-subflow.md)

[Design Assign IP Address Creation subflow](tni-design-assign-ip-address-creation-subflow.md)

[Design assign Logical Connection Creation subflow](tni-design-assign-logical-connection-creation-subflow.md)

[Design Assign Number Element Creation subflow](tni-design-assign-number-element-creation-subflow.md)

[Design Assign Set Attributes subflow](tni-design-assign-set-attributes-subflow.md)

[Design Assign Request Details Update subflow](tni-design-assign-request-details-update-subflow.md)

[Design Assign Connection Element Validation subflow](tni-design-assign-connection-element-validation-subflow.md)

[Design Assign IP Address Validation subflow](tni-design-assign-ip-address-validation-subflow.md)

[Design Assign Number Element Validation subflow](tni-design-assign-number-element-validation-subflow.md)

