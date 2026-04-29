---
title: Define colors for work order states
description: Define colors for work order states so that you can have a visual indication of the task state in the Dispatcher Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Define colors for work order states

Define colors for work order states so that you can have a visual indication of the task state in the Dispatcher Workspace.

## Before you begin

Role required: wm\_admin, admin

The property `work.management.task_state_color.use_hex` must be enabled to change work order tasks state colors.

Define colors for work order states 

## About this task

By default, each work order task state is represented with a specific color. You can change colors for existing work order task states or define a color for a new state. The assigned work order state colors appear in the task card and calendar of Dispatcher Workspace.

You can display events in their selected default color on Dispatcher Workspace calendar by configuring the **sn\_fsm\_disp\_wrkspc.agent\_shift\_schdlng\_event\_color** property. Different events can be created in the Workforce Optimization for Field Service application, such as agent's break, time-off, and more. For more information about property, see [Workforce Optimization for Field Service components](../reference/components-wfo-fsm.md).

## Procedure

1.  Navigate to **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Task State Colors**.

2.  Either select an existing task state or create a new one.

    -   To select the task state whose colors you want to change, select the task state name.
    -   To create a task state, select **New**.
3.  On the form, fill in the form.

    |Field|Description|
    |-----|-----------|
    |Name|Work order task state name.|
    |Primary field value|State of the work order task.|
    |Secondary field value|Substate of the work order task.|
    |Color|Hexadecimal color code.|
    |Active|Option to see the changes in Dispatcher Workspace.|

4.  Select **Submit**.


## Result

The color code is applied to the task state. The color appears in the task card and calendar of Dispatcher Workspace.

