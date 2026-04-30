---
title: Use the InvokeFlow component
description: Invoke or call a flow that is available in Workflow Studio by using the InvokeFlow component of RPA Desktop Design Studio. Generate the context ID of the flow and use the ID in other flow designer components to get the execution status and output.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Flow Designer components, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the InvokeFlow component

Invoke or call a flow that is available in Workflow Studio by using the InvokeFlow component of RPA Desktop Design Studio. Generate the context ID of the flow and use the ID in other flow designer components to get the execution status and output.

## Before you begin

To understand more about flows in Workflow Studio, see [Building flows](https://www.servicenow.com/docs/access?context=flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

Before you use any Flow Designer component, use the Connection Manager to make sure that you're connected to the instance. For more information about how to connect to an instance, [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

Enable the client callable option on an RPA Hub flow or subflow. For more information, see [Enable the client callable option on an RPA Hub flow or subflow](enable-client-flow-rpa.md).

Role required: fd\_read role. For more information on this role, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## About this task

The InvokeFlow component returns the context ID of a flow in Workflow Studio so you can use it in other components. For example, you can use the context ID to get the execution status or the output of a flow.

Add the InvokeFlow component to get the context ID of a flow so other Flow Designer components can check its status or obtain its output. To get the context ID of a subflow, use the InvokeSubFlow component.

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Flow Designer**.

2.  Drag the InvokeFlow component to the Design surface.

3.  On the Design surface, select the Configure button ![Configure icon.](../image/component-settings-icon.png) of the InvokeFlow component to show the InvokeFlow dialog box.

4.  Enter a minimum of three characters to search and select the flow in the **Flow name** field.

    **Important:** You can view and select only those flows that have the application scope set to **All application scopes**. The application scope is set in the **Accessible From** field in your Workflow Studio instance. When the application scope of the flow is set as **This application scope only**, the flow isn't available in the drop-down list of the **Flow name** field.

5.  Verify the input fields, and select **OK**.

6.  Configure the properties of the InvokeFlow component.

    For more information, see [Properties of the Flow Designer components](../reference/properties-flow-designer-components.md).

    You can now connect the **Context ID** port to another Flow Designer component such as GetExecutionStatus or GetOutputs.

7.  To test the component, in the **Design** tab, click **Run**.


**Parent Topic:**[Flow Designer components](../concept/flow-designer-components.md)

