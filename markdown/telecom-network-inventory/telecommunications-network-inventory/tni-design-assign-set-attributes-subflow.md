---
title: TNI Design Assign Set Attributes subflow
description: The TNI Design Assign Set Attributes subflow enables you to update the TNI CI attribute record in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/tni-design-assign-set-attributes-subflow.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Telecommunications Network Inventory subflows, Reference, Telecommunications Network Inventory]
---

# TNI Design Assign Set Attributes subflow

The TNI Design Assign Set Attributes subflow enables you to update the TNI CI attribute record in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.

The TNI Design Assign Set Attributes subflow updates the TNI CI attributes that are associated with a logical connection and updates them in a change task. This subflow functions are as follows.

-   Get the details from the Set attributes activity.
-   Update attributes in TNI CI record.
-   Update change task that is associated with the Set attributes activity.

## Roles and availability

An admin can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the TNI Design Assign Set Attributes subflow and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Change Task|The change task that is associated with Set attributes activity.|Reference.Change Task|
|Ignore Validation Error|Ignores any validation errors.|True/False|

To learn more about the variable data types, see Flow Designer input and output data variables.

## Output

The TNI Design Assign Set Attributes subflow output are as follows.

-   Update attributes in TNI CI record.
-   Update change task that is associated with the Set attributes activity.

**Parent Topic:**[Telecommunications Network Inventory subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/subflow.md)

**Related topics**  


[Create Logical Connection with template subflow]()

[Logical Connection Creation subflow]()

[Physical connection creation subflow]()

[TNI Design Assign Connection Element Creation subflow]()

[TNI Design Assign Protected Path Assignment subflow]()

[TNI Design Assign IP Address Creation subflow]()

[TNI Design assign Logical Connection Creation subflow]()

[TNI Design Assign Number Element Creation subflow]()

[TNI Design Assign Request Details Update subflow]()

[TNI Design Assign Connection Element Validation subflow]()

[TNI Design Assign IP Address Validation subflow]()

[TNI Design Assign Number Element Validation subflow]()

