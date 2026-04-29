---
title: Enable the client callable option on a flow or subflow in RPA Hub
description: Enable a client script to trigger an RPA Hub flow or subflow.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions and subflow, Use, RPA Hub, Workflow Data Fabric]
---

# Enable the client callable option on a flow or subflow in RPA Hub

Enable a client script to trigger an RPA Hub flow or subflow.

## Before you begin

You must do this task in the classic environment.

Make sure that you're familiar with the RPA Hub actions and subflow. For more information, see [Workflow Studio actions and subflow in RPA Hub](../../rpa-hub/reference/rpa-hub-actions.md).

Invoke a flow or a subflow from Workflow Studio by using the InvokeFlow component or InvokeSubFlow component. For more information, see [Use the InvokeFlow component](use-rpahub-flowdesigner-invokeflow.md) and [Use the InvokeSubFlow component](use-rpahub-flowdesigner-invokesubflow.md).

By default, the flows, subflows, and actions can only be called by the FlowAPI within a server script. Flow and action designers can make individual flows, subflows, or actions available to client calls by enabling the Client callable option during design.

Consider the implications of making a flow or subflow client callable, such as whether it exposes protected data or bypasses validation logic.

Role required: security\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Open the flow or subflow that you want to make the client callable on.

3.  In the More Actions menu, select **Manage security**.

4.  Select **Callable by Client API**.

5.  Add the RPA Flow Designer ACL record that you created earlier to the **ACLs** field.

6.  Select **Update**.


**Parent Topic:**[Workflow Studio actions and subflow in RPA Hub](../../rpa-hub/reference/rpa-hub-actions.md)

