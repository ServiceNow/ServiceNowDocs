---
title: Design Assign Connection Element Creation subflow
description: The TNI Design Assign Connection Element Creation subflow enables you to create the connection element records in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/tni-design-assign-connection-element-creation-subflow.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Subflows, Reference, Telecommunications Network Inventory]
---

# Design Assign Connection Element Creation subflow

The TNI Design Assign Connection Element Creation subflow enables you to create the connection element records in the Telecommunications Network Inventory application. You can use this flow action to configure the activities in a Design and Assign playbook for logical connection.

The TNI Design Assign Connection Element Creation subflow creates the connection elements that are associated with a logical connection and updates them in a change task. This subflow functions are as follows.

-   Get the details from the Define end points and Setup logical connection activities.
-   Create connection elements.
-   Check whether the start/end equipment matches with the start/end port.
-   Create CI relationships if the equipment matches with the port.
-   Update change task that is associated with the Assign connection element activity.

## Roles and availability

An admin can add a subflow to a flow and define the configuration details of the flow. This Workflow Studio subflow is available in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the TNI Design Assign Connection Element Creation subflow and their descriptions.

|Field Name|Description|Data Type|
|----------|-----------|---------|
|Change Task|The change task that is associated with Assign connection element activity.|Reference.Change Task|
|Ignore Validation Error|Ignores any validation errors.|True/False|

To learn more about the variable data types, see Flow Designer input and output data variables.

## Output

The TNI Design Assign Connection Element Creation subflow output are as follows.

-   Create the connection elements.
-   Create the CI relationship between equipment and port.
-   Update the change task that is associated with the Assign connection element activity.

**Parent Topic:**[Telecommunications Network Inventory subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/subflow.md)

**Related topics**  


[Create Logical Connection with template subflow]()

[Logical Connection Creation subflow]()

[Physical connection creation subflow]()

[Design Assign Protected Path Assignment subflow]()

[Design Assign IP Address Creation subflow]()

[Design assign Logical Connection Creation subflow]()

[Design Assign Number Element Creation subflow]()

[Design Assign Set Attributes subflow]()

[Design Assign Request Details Update subflow]()

[Design Assign Connection Element Validation subflow]()

[Design Assign IP Address Validation subflow]()

[Design Assign Number Element Validation subflow]()

