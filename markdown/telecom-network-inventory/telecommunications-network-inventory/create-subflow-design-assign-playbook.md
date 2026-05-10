---
title: Create subflow for Design and Assign function
description: Create a subflow in the Workflow Studio. You can use this subflow to configure an activity in the playbook for the Design and Assign function.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Design and Assign function, Configure, Telecommunications Network Inventory]
---

# Create subflow for Design and Assign function

Create a subflow in the Workflow Studio. You can use this subflow to configure an activity in the playbook for the Design and Assign function.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

You create a subflow by defining the input data that the subflow uses and the output data it generates. Then you link the subflow to a request definition. You can use this request definition to configure an activity to automate the design and assign function using a playbook. The subflows associated with request definitions are triggered by the TNI Design Assign process flow after you submit them.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **New** and then select **Subflow** from the option list.

3.  Fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |Subflow name|Name of the subflow.|
    |Description|Description of the subflow.|
    |Application|Application scope to create the subflow in. You can select **Network Inventory Advanced**.|

4.  Create the subflow input and assign an appropriate value to the subflow output according to your requirement.

    To learn more, see [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-subflow.md).

    **Note:** The subflows are triggered by the TNI Design Assign process flow on submission, and the following inputs are required.

    -   Ignore validation error
    -   Change task

## What to do next

-   Test the subflow, and publish it when it’s ready to be added to the record producer.
-   Create a request definition and associate the subflow. To learn more, see [Create a request definition for Design and Assign function](create-request-definition-design-assign-function.md).

**Parent Topic:**[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

**Related topics**  


[Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md)

[Telecommunications Network Inventory subflows](../concept/subflow.md)

[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

[Configure a Design and Assign function example](../concept/configure-design-assign-playbook-use-case.md)

