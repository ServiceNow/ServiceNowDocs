---
title: Use the InvokeAction component
description: The InvokeAction component returns the context ID of an action in Workflow Studio so you can use it in other components. For example, you can use the context ID to get the execution status or the output of an action.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Flow Designer components, ServiceNow, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the InvokeAction component

The InvokeAction component returns the context ID of an action in Workflow Studio so you can use it in other components. For example, you can use the context ID to get the execution status or the output of an action.

## Before you begin

To understand more about flows in Workflow Studio, see [Building flows](https://www.servicenow.com/docs/access?context=flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

Before you use any Flow Designer component, use the Connection Manager to make sure that you're connected to the instance. For more information about how to connect to an instance, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

Enable the client callable option on an RPA Hub flow or subflow. For more information, see [Enable the client callable option on a flow or subflow in RPA Hub](enable-client-flow-rpa.md).

Role required: fd\_read role. For more information on this role, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## About this task

Add the InvokeAction component to get the context ID of an action so other Flow Designer components can check its status or obtain its output. To get the context ID of a flow or a subflow, use the InvokeFlow component or the InvokeSubFlow component.

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Flow Designer**.

2.  Drag the InvokeAction component to the Design surface.

3.  On the Design surface, select the Configure button ![Configure icon.](../image/component-settings-icon.png) of the InvokeAction component to show the InvokeAction dialog box.

4.  In the **Action name** field, enter a minimum of three characters to search and select Enter.

    A list of actions that start with the entered characters is shown from the connected ServiceNow instance.

    **Important:** You can view and select only those actions that have the application scope set to **All application scopes**. The application scope is set in the **Accessible From** field in your Workflow Studio instance. When the application scope of the action is set as **This application scope only**, the action isn’t available in the drop-down list from the **Action name** field.

5.  Select the required action from the search list.

6.  Verify the input fields, and select **OK**.

7.  Configure the properties of the InvokeSubFlow component.

    For more information, see [Properties of the Flow Designer components](../reference/properties-flow-designer-components.md).

    You can now connect the **Context ID** port to another Flow Designer component such as GetExecutionStatus or GetOutputs.

8.  To test the component, in the **Design** tab, select **Run**.


**Parent Topic:**[Flow Designer components](../concept/flow-designer-components.md)

