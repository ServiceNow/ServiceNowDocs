---
title: Use the GetExecutionStatus component
description: Use the GetExecutionStatus component to determine the execution status of a flow or a subflow in Workflow Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flow Designer components, ServiceNow, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetExecutionStatus component

Use the GetExecutionStatus component to determine the execution status of a flow or a subflow in Workflow Studio.

## Before you begin

To understand more about flows in Workflow Studio, see Building flows.

Before you use any Flow Designer component, use the Connection Manager to make sure that you're connected to the instance. For more information about how to connect to an instance, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

Role required: none

## About this task

Before you use the GetOutputs component to get the output of a flow, you may want to check the flow's status. When a flow has executed successfully, the execution status is COMPLETE. When the execution status is other than COMPLETE, the GetOutputs component may not obtain a helpful result.

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Flow Designer**.

2.  Drag the GetExecutionStatus component to the Design surface.

3.  Configure the component properties by using the Properties pane.

    For example, you can configure the component to include a timeout or a delay before the component executes. For more information about these properties, see [Properties of the Flow Designer components](../reference/properties-flow-designer-components.md).

4.  Connect the data and control ports of the GetExecutionStatus component to the corresponding ports of other components as described in the following table.

    |Parameter|Description|Data port type|Data type|Required?|
    |---------|-----------|--------------|---------|---------|
    |ContextID|Receives a context ID from the InvokeFlow, InvokeSubFlow, or InvokeAction component|Data In|String|Yes|
    |Status|Returns the execution status and passes it to the next component|Data Out|String|Yes|

    To view the execution status in RPA Desktop Design Studio, right-click the **Status** field and select **Preview Data**.

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Flow Designer components](../concept/flow-designer-components.md)

