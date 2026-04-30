---
title: Event-specific workflow activities
description: The following workflow activities trigger events.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow events in the base system, Workflow events, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Event-specific workflow activities

The following workflow activities trigger events.

<table id="table_pmc_twt_hp"><thead><tr><th>

Activity Name

</th><th>

Description

</th><th>

Purpose

</th><th>

To Use

</th><th>

Source

</th><th>

Thread

</th><th>

Listeners

</th></tr></thead><tbody><tr><td>

Create Event

</td><td>

Requires an event from the event registry rather than a workflow event. This activity is located in the **Notification** category of the workflow tree.

</td><td>

Fires the notification event specified in the Workflow Activity \[wf\_activity\] table.

</td><td>

1.  Navigate to **System Policy** &gt; **Events** &gt; **Registry**
2.  Create an event.
3.  Navigate to **System Policy** &gt; **Templates** and create an [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
4.  Navigate to **System Policy** &gt; **Email** &gt; **Notifications**.
5.  [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) that is triggered by the event you created and sends the template you created.
6.  On the workflow canvas, drag the **Create Event** activity onto the canvas and associate it with the newly registered event.

When the workflow executes, the event is created and the email associated with the event is sent.

</td><td>

Event Registry

</td><td>

Triggered in the current thread and handled on the worker thread in notifications. Never processed by a workflow

</td><td>

On the notification thread, outside of workflow

</td></tr><tr><td>

[Wait for WF Event](../../workflow-activities/reference/r_WaitForWFEvent.md)

</td><td>

Listens for workflow events, as described in the [Workflow Events in the Base System](r_WorkflowEventsInTheBaseSystem.md) table, and only within the current context. This activity is located in the **Conditions** category of the workflow tree.

</td><td>

Waits for another transition branch of the current context to trigger an event.

</td><td>

Takes an event name as input. When the activity is executed, the specified event name is added to a string array stored in the **registered\_events** column. The values in this column are in a list of all events the activity waits for when it is executing.

</td><td>

The **Wait for WF Event** activity has a generic onUnhandledEvent that tests the current event against the value that was passed to the variable. If they match, the **Wait for WF Event** moves the workflow forward.

</td><td>

Triggered in the current thread or from a script include

</td><td>

The onUnhandledEvent of the **Wait for WF Event** activity

</td></tr></tbody>
</table>**Parent Topic:**[Workflow events in the base system](r_WorkflowEventsInTheBaseSystem.md)

