---
title: Manage work order tasks
description: Track and monitor the real-time state of work order tasks. You can auto-assign tasks, record time, request more information, and cancel the work order task.Assign a work order task to a field service agent from Dispatcher Workspace.As a dispatcher, you can recommend the best available tasks to fill gaps in an agent's schedule.Record the duration for executing a task using the Dispatcher Workspace application.Cancel a work order task in Dispatcher Workspace if it is no longer necessary or is a duplicate of another work order task.Suspend the parent work order of a task to stop displaying active SLAs for the task, including the time remaining, the SLA state, and any breaches.Assign work order tasks directly to the outsourced service providers \(also called contractor companies\) from an external assignment group using Dispatcher Workspace.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Using Dispatcher Workspace, Assigning work order tasks to agents from Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Manage work order tasks

Track and monitor the real-time state of work order tasks. You can auto-assign tasks, record time, request more information, and cancel the work order task.

## Assign work order tasks to agents

Assign a work order task to a field service agent from Dispatcher Workspace.

### Before you begin

Role required: wm\_dispatcher

If the time required to complete the task needs multiple schedule entries or days, select the **Assign across the schedule entries** option in the work order task form.

If the task is assigned to an agent in the territory that best match its location then you must enable the following options:

-   The Field Service territory model, **Field\_Service\_Territories**. For more information, see [Enable the Field Service territory model](../task/enable-territory-model.md).
-   **Territory** option in Dispatcher Workspace to view the territory information in the task card and the agent card. For more information, see [Enable Dispatcher Workspace settings](../task/dispatcher-wrkspc-settings.md).

If the task assignment method needs to respect the workforce optimized shift schedules then you must enable the **Enable Shift Scheduling for FSM to Determine Availability** configuration to activate the Workforce Optimization for Field Service data model. For more information, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

**Note:** If the **Enable Shift Scheduling for FSM to Determine Availability** configuration is enabled, the Dispatcher Workspace calendar displays the schedules and events created in Workforce Optimization for Field Service application.

### About this task

You can assign work order tasks that are in pending to dispatch either manually or automatically in the Dispatcher Workspace.

-   To assign work order tasks automatically, you must enable dynamic scheduling. The auto-assign capability automatically matches a task to a nearby agent who has the necessary skills and a schedule that can accommodate the task. For more information, see [Setting up dynamic scheduling in Dispatcher Workspace](dispatcher-ws-dy-scheduling.md).
-   To assign work order tasks manually, consider the following aspects:
    -   The length of time required to complete a task
    -   The window of time in which a task must be completed
    -   The schedule and availability of agents with the necessary skill sets
    -   The availability of agents with required skill sets if configured
    -   The availability of required parts
    -   The impact on other tasks
    -   The agent task route map

If an agent is part of more than one assignment group or territory, then dispatchers will see the agent on more than one line on the calendar in Dispatcher Workspace. To change the agent’s schedule, the dispatcher must make changes on the line that corresponds with the assignment group or territory they manage.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

    **Note:** You can sort, filter, and also match the work order tasks based on the calendar dates before assigning field service agents. For more information, see [Search work order tasks](../task/search-work-order-tasks.md) and [Search for appropriate Field Service agents](../task/search-agents-tasks.md).

3.  Assign the work order task to agents.

<table id="choicetable_sbq_vhp_b4b"><thead><tr><th align="left" id="d25326e292">

To

</th><th align="left" id="d25326e295">

Do this

</th></tr></thead><tbody><tr><td id="d25326e301">

**Assign a task manually from the task panel**

</td><td>

1.  Select the task from the task panel.
2.  Drag the task to the calendar slot of an agent who is close to the task location.
3.  Select **Save**.


</td></tr><tr><td id="d25326e325">

**Assign a task manually from the contextual side panel**

</td><td>

1.  Select the Open info \(![open info](../image/open-info.png)\) icon on a task in the task panel.
2.  Select the Overflow actions\(![overflow actions](../image/overflow-actions.png)\) icon in the contextual side panel.
3.  Select **Assign**.
4.  In the **Assigned to** field, select the agent you want to assign the task to.
5.  Select **Save**.


</td></tr><tr><td id="d25326e373">

**Assign a task manually from the dispatch map**

</td><td>

1.  Right-click a task in the dispatch map.
2.  Select **Assign**.
3.  In the **Assigned to** field, select the agent you want to assign the task to.
4.  Select **Save**.


</td></tr><tr><td id="d25326e406">

**Auto-assign a task from the task panel**

</td><td>

1.  Select the more actions icon \(![More actions icon](../image/more_actions.png)\) on the task card.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d25326e440">

**Auto-assign a task from the contextual side panel**

</td><td>

1.  Select the Open info \(![open info](../image/open-info.png)\) icon on a task in the task panel.
2.  Select the Overflow actions \(![overflow actions](../image/overflow-actions.png)\) icon in the contextual side panel.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr><tr><td id="d25326e482">

**Auto-assign from the task record**

</td><td>

1.  Select a work order task from the task panel.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d25326e509">

**Auto-assign a task from a list**

</td><td>

1.  Select the List icon \( ![List icon.](../image/lists_icon.png)\) and select **My Dispatch Queue**.
2.  Select the work order task.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr><tr><td id="d25326e548">

**Auto-assign a task from the dispatch map**

</td><td>

1.  Right-click a task in the dispatch map.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr></tbody>
</table>
### Result

The task is assigned to an agent. The following then happens:

-   The task is displayed on the calendar next to the agent's name. The work order task color appears in the color as defined for assigned tasks.
-   The **Assigned to** field in the work order task contains the agent's name.
-   If a task is assigned to an agent, the system updates the estimated travel duration based on the agent's home location. The updated value is based on the **Manual Assignment** property setting used for calculating estimated travel time and distance.

There can be issues with the task assignment, such as the following:

-   If the assigned task is outside the acceptable radius between the task location and the agent's location, a warning message appears.
-   If the agent doesn’t accept in a specific time period, the work order task is automatically rejected. The dispatcher can reassign the task to other available agents.

## Assign work order tasks to agents using Intelligent Task Recommendation

As a dispatcher, you can recommend the best available tasks to fill gaps in an agent's schedule.

### Before you begin

Role required: wm\_dispatcher

Ensure the Field Service Intelligent Task Recommendation plugin is activated. For more information, see [Activate Intelligent Task Recommendation](../task/activate-intelligent-task-recommendation.md).

### About this task

The Intelligent Task Recommendation feature identifies and recommends the best available tasks for agents based on the selected start time and end time based on the following.

-   Excludes the work order tasks that are schedule locked.
-   Considers the agent's start and end locations from the**Agent Schedule Attribute Plans** table for the given day if the Territory Planning plugin is activated.
-   Integrates agent's schedule and events from the Workforce Optimization for Field Service application if the **Enable Shift Scheduling for FSM to Determine Availability** configuration is enabled. For more information, see [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md) and [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click **Dispatcher Workspace**.

3.  In the calendar, select a date to view an agent's schedule for that day.

4.  Select the white space that indicates the gap in the agent's calendar.

    The Recommended tasks dialog box displays the maximum five best available tasks for the agent. The tasks are arranged in descending order based on their recommendation score.

5.  From the Recommended tasks list, select the task that you want to assign to the agent.

6.  Click **Assign**.


### Result

The recommended task is assigned to the agent. The agent receives a push notification that the work order task has been assigned.

## Record time spent on a task

Record the duration for executing a task using the Dispatcher Workspace application.

### Before you begin

Role required: wm\_dispatcher

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click a task number from the task panel or calendar.

3.  Click **Record Time**.

4.  In the **User** field, select an agent for whom you want to record time.

5.  Enter the time worked.

    |Field|Description|
    |-----|-----------|
    |Days|Number of days worked on the task.|
    |Time Worked \(Hours\)|Number of hours worked on the task.|
    |Time Worked \(Minutes\)|Number of minutes worked on the task.|

6.  In the Comments field, enter any additional notes about the task.

7.  Click **Save**.


### Result

The time card is automatically created for the user.

## Cancel a work order task in Dispatcher Workspace

Cancel a work order task in Dispatcher Workspace if it is no longer necessary or is a duplicate of another work order task.

### Before you begin

Role required: wm\_dispatcher

### About this task

Work orders and work order tasks cannot be canceled that are in the **Closed Complete** or **Closed Incomplete** state.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click a task number from the task panel or calendar panel.

3.  Click **Cancel Task**.

4.  In the **Work notes** field, enter a cancellation reason.

    An error message appears if text is not entered.


### Result

The customer receives an SMS and email notification that the work order task is canceled.

## Suspend the parent work order of a task

Suspend the parent work order of a task to stop displaying active SLAs for the task, including the time remaining, the SLA state, and any breaches.

### Before you begin

Role required: wm\_dispatcher.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click a task number from the task panel or calendar panel.

3.  Click **Suspend Parent**.

4.  In the **Work notes** field, enter the reason to suspend.

    An error message appears if text is not entered.

5.  Click **Post Work notes**.


### Result

The parent work order of the task is suspended.

## Assign work order task to an outsourced service provider in Dispatcher Workspace

Assign work order tasks directly to the outsourced service providers \(also called contractor companies\) from an external assignment group using Dispatcher Workspace.

### Before you begin

Role required: wm\_dispatcher

-   Activate the Field Service Contractor Management \(com.snc.fsm\_contractor\_management\) plugin.
-   Add external vendor assignment groups to the dispatch group. For more information, see [Add external assignment groups to the dispatch group](../task/add-external-assignment-group-to-disp-group.md).

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click **Dispatcher Workspace**.

3.  Click a task from the task panel and drag it to the calendar slot of an outsourced service provider in the Contractor groups.

    Acme Services

    The Assignment confirmation dialog box is displayed.

4.  Click **Save**.


### Result

-   The task is displayed on the calendar next to the outsourced service provider's name.
-   The task is assigned to the manager of the outsourced service provider.
-   The calendar view of the outsourced service provider displays the capacity utilization information in percentage and definition. For example, if company's defined capacity is five tasks and so far only two tasks are assigned to the company, the capacity utilization data displays that 40% capacity has been utilized and 2 out of 5 tasks have been assigned to the company. For more information about capacity reservation rules, see [Capacity and Reservations Management](capacity-management.md).
-   If the tasks assigned to the outsourced service provider is more than its defined capacity, a red vertical bar displays on the calendar, indicating over-allocation of tasks.

