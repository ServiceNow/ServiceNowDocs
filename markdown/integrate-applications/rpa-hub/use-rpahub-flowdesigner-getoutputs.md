---
title: Use the GetOutputs component
description: Use the GetOutputs component to get the output of a flow or a subflow in Workflow Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Flow Designer components, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetOutputs component

Use the GetOutputs component to get the output of a flow or a subflow in Workflow Studio.

## Before you begin

To understand more about flows in Workflow Studio, see [Building flows](https://www.servicenow.com/docs/access?context=flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

Before you use any Flow Designer component, use the Connection Manager to make sure that you're connected to the instance. For more information about how to connect to an instance, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

Use the GetExecutionStatus component to know the execution status of the flow or subflow. To use the component, see [Use the GetExecutionStatus component](use-rpahub-flowdesigner-getexecutionstatus.md).

Role required: none

## About this task

There are many reasons why you might want to receive the output of a flow. For example, suppose you have an automation that includes an incident number, and you want to obtain the incident’s description. You can use Workflow Studio to create a flow that takes the incident number as input and returns the description. Then, in RPA Desktop Design Studio, you can invoke the flow using the InvokeFlow component and send its context ID to the GetOutputs component to get the output, including the incident description.

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Flow Designer**.

2.  Drag the GetOutputs component to the Design surface.

3.  Configure the component properties by using the Properties pane.

    For example, you can configure the component to include a timeout or a delay before the component executes. For more information about these properties, see [Properties of the Flow Designer components](../reference/properties-flow-designer-components.md).

4.  Connect the data and control ports of the GetOutputs component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Purpose of connection

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Data In \(Context ID\)

</td><td>

Receives a context ID from the InvokeFlow, InvokeSubFlow, or InvokeAction component

</td><td>

Yes

</td></tr><tr><td>

Data Out \(Return\)

</td><td>

Returns the output of the flow, subflow, or action and passes it to the next component

</td><td>

Yes.To view the output, right-click the **Return** field and click **Preview Data**.

</td></tr><tr><td>

Control In

</td><td>

Passes the control from the previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Control Out

</td><td>

Passes the control to the next component to be executed.

</td><td>

No. Connecting this port is optional.

</td></tr></tbody>
</table>    To view the output in RPA Desktop Design Studio, right-click the **Return** field and select **Preview Data**.

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Flow Designer components](../concept/flow-designer-components.md)

