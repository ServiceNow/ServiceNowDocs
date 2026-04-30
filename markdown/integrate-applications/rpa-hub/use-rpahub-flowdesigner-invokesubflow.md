---
title: Use the InvokeSubFlow component
description: The InvokeSubFlow component returns the context ID of a subflow in Workflow Studio so you can use it in other components. For example, you can use the context ID to get the execution status or the output of a subflow.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Flow Designer components, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the InvokeSubFlow component

The InvokeSubFlow component returns the context ID of a subflow in Workflow Studio so you can use it in other components. For example, you can use the context ID to get the execution status or the output of a subflow.

## Before you begin

To understand more about flows in Workflow Studio, see [Building flows](https://www.servicenow.com/docs/access?context=flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

Before you use any Flow Designer component, use the Connection Manager to make sure that you're connected to the instance. For more information about how to connect to an instance, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

Enable the client callable option on an RPA Hub flow or subflow. For more information, see [Enable the client callable option on an RPA Hub flow or subflow](enable-client-flow-rpa.md).

Role required: fd\_read role. For more information on this role, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## About this task

Add the InvokeSubFlow component to get the context ID of a subflow so other Flow Designer components can check its status or obtain its output. To get the context ID of a flow, use the InvokeFlow component.

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Flow Designer**.

2.  Drag the InvokeSubFlow component to the Design surface.

3.  On the Design surface, select the Configure button ![Configure icon.](../image/component-settings-icon.png) of the InvokeSubFlow component to show the InvokeSubFlow dialog box.

4.  In the **Subflow name** field, enter a minimum of three characters to search and select Enter.

    A list of subflows that start with the entered characters is shown from the connected ServiceNow instance.

    **Important:** You can view and select only those subflows that have the application scope set to **All application scopes**. The application scope is set in the **Accessible From** field in your Workflow Studio instance. When the application scope of the subflow is set as **This application scope only**, the subflow isn’t available in the drop-down list of the **Subflow name** field.

5.  Select the required subflow from the search list.

6.  Verify the input fields, and select **OK**.

7.  Configure the properties of the InvokeSubFlow component.

    For more information, see [Properties of the Flow Designer components](../reference/properties-flow-designer-components.md).

    You can now connect the **Context ID** parameter with other Flow Designer components such as GetExecutionStatus or GetOutputs

8.  To test the component, in the **Design** tab, select **Run**.


**Parent Topic:**[Flow Designer components](../concept/flow-designer-components.md)

