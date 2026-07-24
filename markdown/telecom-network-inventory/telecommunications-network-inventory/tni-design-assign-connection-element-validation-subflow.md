---
title: Design Assign Connection Element Validation subflow
description: The TNI Design Assign Connection Element Validation subflow enables you to validate the connection element records in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/tni-design-assign-connection-element-validation-subflow.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Subflows, Reference, Telecommunications Network Inventory]
---

# Design Assign Connection Element Validation subflow

The TNI Design Assign Connection Element Validation subflow enables you to validate the connection element records in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.

The TNI Design Assign Connection Element Validation subflow validates whether the connection element records required for the Assign connection element activity have already been used or not. If the connection elements are already used, the subflow passes the information.

## Roles and availability

An admin can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the TNI Design Assign Connection Element Validation subflow and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Change Task|The change task that is associated with Assign connection element activity.|Reference.Change Task|
|Ignore Validation Error|Ignores any validation errors.|True/False|

To learn more about the variable data types, see Flow Designer input and output data variables.

## Output

If the connection element is already used, then the subflow passes the following message "**The connection element has already been fully used. Please try creating another one.**"

**Parent Topic:**[Telecommunications Network Inventory subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/subflow.md)

**Related topics**  


[Create Logical Connection with template subflow]()

[Logical Connection Creation subflow]()

[Physical connection creation subflow]()

[Design Assign Connection Element Creation subflow]()

[Design Assign Protected Path Assignment subflow]()

[Design Assign IP Address Creation subflow]()

[Design assign Logical Connection Creation subflow]()

[Design Assign Number Element Creation subflow]()

[Design Assign Set Attributes subflow]()

[Design Assign Request Details Update subflow]()

[Design Assign IP Address Validation subflow]()

[Design Assign Number Element Validation subflow]()

