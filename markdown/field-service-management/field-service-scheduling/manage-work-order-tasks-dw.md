---
title: Manage work order tasks
description: Track and monitor the real-time state of work order tasks. You can auto-assign tasks, record time, request more information, and cancel the work order task.Assign a work order task to a field service agent from Dispatcher Workspace.As a dispatcher, you can recommend the best available tasks to fill gaps in an agent's schedule.Record the duration for executing a task using the Dispatcher Workspace application.Cancel a work order task in Dispatcher Workspace if it’s no longer necessary or is a duplicate of another work order task.Suspend the parent work order of a task to stop displaying active SLAs for the task, including the time remaining, the SLA state, and any breaches.Assign work order tasks directly to the outsourced service providers \(also called contractor companies\) from an external assignment group using Dispatcher Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/manage-work-order-tasks-dw.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Manage work order tasks

Track and monitor the real-time state of work order tasks. You can auto-assign tasks, record time, request more information, and cancel the work order task.

## Assign work order tasks to agents

Assign a work order task to a field service agent from Dispatcher Workspace.

### Before you begin

Role required: wm\_dispatcher

If the time required to complete the task needs multiple schedule entries or days, select the **Assign across the schedule entries** option in the work order task form.

If the task is assigned to an agent in the territory that best matches its location, then you must enable the following options:

-   The Field Service territory model, **Field\_Service\_Territories**. For more information, see [Enable the Field Service territory model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/enable-territory-model.md).
-   **Territory** option in Dispatcher Workspace to view the territory information in the task card and the agent card. For more information, see [Enable Dispatcher Workspace settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/dispatcher-wrkspc-settings.md).

If the task assignment method must respect the workforce optimized shift schedules then you must enable the **Enable Shift Scheduling for FSM to Determine Availability** configuration to activate the Workforce Optimization for Field Service data model. For more information, see [Activate Workforce Optimization for Field Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/activate-wfo-fsm.md).

**Note:** If the **Enable Shift Scheduling for FSM to Determine Availability** configuration is enabled, the Dispatcher Workspace calendar displays the schedules and events created in Workforce Optimization for Field Service application.

### About this task

You can assign work order tasks that are in pending to dispatch either manually or automatically in the Dispatcher Workspace.

-   To assign work order tasks automatically, you must enable dynamic scheduling. The auto-assign capability automatically matches a task to a nearby agent who has the necessary skills and a schedule that can accommodate the task. For more information, see [Setting up dynamic scheduling in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/dispatcher-ws-dy-scheduling.md).
-   To assign work order tasks manually, consider the following aspects:
    -   The length of time required to complete a task
    -   The window of time in which a task must be completed
    -   The schedule and availability of agents with the necessary skill sets
    -   The availability of agents with required skill sets if configured
    -   The availability of required parts
    -   The impact on other tasks
    -   The agent task route map

If an agent is part of more than one assignment group or territory, then dispatchers see the agent on more than one line on the calendar in Dispatcher Workspace. To change the agent’s schedule, the dispatcher must change the line that corresponds with the assignment group or territory they manage.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

    **Note:** You can sort, filter, and also match the work order tasks based on the calendar dates before assigning field service agents. For more information, see [Search work order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/search-work-order-tasks.md) and [Search for appropriate Field Service agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/search-agents-tasks.md).

3.  Assign the work order task to agents.

<table id="choicetable_sbq_vhp_b4b"><thead><tr><th align="left" id="d27969e309">

To

</th><th align="left" id="d27969e312">

Do this

</th></tr></thead><tbody><tr><td id="d27969e318">

**Assign a task manually from the task panel**

</td><td>

1.  Select the task from the task panel.
2.  Drag the task to the calendar slot of an agent who is close to the task location.
3.  Select **Save**.


</td></tr><tr><td id="d27969e342">

**Assign a task manually from the contextual side panel**

</td><td>

1.  Select the Open info \(\[Omitted image "open-info.png"\] Alt text: open info\) icon on a task in the task panel.
2.  Select the Overflow actions\(\[Omitted image "overflow-actions.png"\] Alt text: overflow actions\) icon in the contextual side panel.
3.  Select **Assign**.
4.  In the **Assigned to** field, select the agent you want to assign the task to.
5.  Select **Save**.


</td></tr><tr><td id="d27969e390">

**Assign a task manually from the map**

</td><td>

1.  Select and hold \(or right-click\) a task in the map.
2.  Select **Assign**.
3.  In the **Assigned to** field, select the agent you want to assign the task to.
4.  Select **Save**.


</td></tr><tr><td id="d27969e423">

**Auto-assign a task from the task panel**

</td><td>

1.  Select the more actions icon \(\[Omitted image "more\_actions.png"\] Alt text: More actions icon\) on the task card.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d27969e457">

**Auto-assign a task from the contextual side panel**

</td><td>

1.  Select the Open info \(\[Omitted image "open-info.png"\] Alt text: open info\) icon on a task in the task panel.
2.  Select the Overflow actions \(\[Omitted image "overflow-actions.png"\] Alt text: overflow actions\) icon in the contextual side panel.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr><tr><td id="d27969e499">

**Auto-assign from the task record**

</td><td>

1.  Select a work order task from the task panel.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d27969e526">

**Auto-assign a task from a list**

</td><td>

1.  Select the List icon \( \[Omitted image "lists\_icon.png"\] Alt text: List icon.\) and select **My Dispatch Queue**.
2.  Select the work order task.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr><tr><td id="d27969e565">

**Auto-assign a task from the map**

</td><td>

1.  Select and hold \(or right-click\) a task in the map.
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

The Field Service Intelligent Task Recommendation plugin must be activated. For more information, see [Activate Intelligent Task Recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/activate-intelligent-task-recommendation.md).

### About this task

Intelligent Task Recommendations identifies and recommends the best available tasks for agents based on the following.

-   Start and end time of the task.
-   Excludes the work order tasks that are schedule locked.
-   Agent's territory and task's territory if Field Service Territory Planning plugin \(com.snc.fsm\_territory\_planning\) is enabled.
-   Considers the agent's start and end locations from the **Resource Schedule Attributes** table for the given day.
-   Integrates agent's schedule and events from the Workforce Optimization for Field Service application when the **Enable Shift Scheduling for FSM to Determine Availability** configuration is enabled. For more information, see [Global domain configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/t_ConfigureFieldService.md) and [Activate Workforce Optimization for Field Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/activate-wfo-fsm.md).
-   Considers technician-demand channel association when **Enable Shift Scheduling for FSM to Determine Availability**, **Enable/disable association of territory resources with demand channels**, and territory model is enabled.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  In the calendar, select a date to view an agent's schedule for that day.

4.  Select the white space that indicates the gap in the agent's calendar.

    The Recommended tasks dialog box displays the maximum five best available tasks for the agent. The tasks are arranged in descending order based on their recommendation score.

5.  From the Recommended tasks list, select the task that you want to assign to the agent.

6.  Select **Assign**.


### Result

The recommended task is assigned to the agent. The agent receives a push notification that the work order task has been assigned.

**Related topics**  


[Intelligent Task Recommendation]()

[Configuring Intelligent Task Recommendations]()

[Assign tasks to yourself based on Intelligent Task Recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/recommend-task-fsm-mobile.md)

## Record time spent on a task

Record the duration for executing a task using the Dispatcher Workspace application.

### Before you begin

Role required: wm\_dispatcher

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select a task number from the task panel or calendar.

3.  Select **Record Time**.

4.  In the **User** field, select an agent for whom you want to record time.

5.  Enter the time worked.

    |Field|Description|
    |-----|-----------|
    |Days|Number of days worked on the task.|
    |Time Worked \(Hours\)|Number of hours worked on the task.|
    |Time Worked \(Minutes\)|Number of minutes worked on the task.|

6.  In the Comments field, enter any additional notes about the task.

7.  Select **Save**.


### Result

The time card is automatically created for the user.

## Cancel a work order task in Dispatcher Workspace

Cancel a work order task in Dispatcher Workspace if it’s no longer necessary or is a duplicate of another work order task.

### Before you begin

Role required: wm\_dispatcher

### About this task

Work orders and work order tasks can't be canceled that are in the **Closed Complete** or **Closed Incomplete** state.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select a task number from the task panel or calendar panel.

3.  Select **Cancel Task**.

4.  In the **Work notes** field, enter a cancellation reason.

    An error message appears if text isn’t entered.


### Result

The customer receives an SMS and email notification that the work order task is canceled.

## Suspend the parent work order of a task

Suspend the parent work order of a task to stop displaying active SLAs for the task, including the time remaining, the SLA state, and any breaches.

### Before you begin

Role required: wm\_dispatcher.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select a task number from the task panel or calendar panel.

3.  Select **Suspend Parent**.

4.  In the **Work notes** field, enter the reason to suspend.

    An error message appears if text isn’t entered.

5.  Select **Post Work notes**.


### Result

The parent work order of the task is suspended.

## Assign work order task to an outsourced Service Provider in Dispatcher Workspace

Assign work order tasks directly to the outsourced service providers \(also called contractor companies\) from an external assignment group using Dispatcher Workspace.

### Before you begin

Role required: wm\_dispatcher

-   Activate the Field Service Contractor Management \(com.snc.fsm\_contractor\_management\) plugin.
-   Add external vendor assignment groups to the dispatch group. For more information, see [Add external assignment groups to the dispatch group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/add-external-assignment-group-to-disp-group.md).

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Select a task from the task panel and drag it to the calendar slot of an outsourced service provider in the Contractor groups.

    Acme Services

    The Assignment confirmation dialog box is displayed.

4.  Select **Save**.


### Result

-   The task is displayed on the calendar next to the outsourced service provider's name.
-   The task is assigned to the manager of the outsourced service provider.
-   The calendar view of the outsourced service provider displays the capacity utilization information in percentage and definition. For example, if a company's defined capacity is five tasks and so far only two tasks are assigned to the company, the capacity utilization data displays that 40% capacity has been used and 2 out of 5 tasks have been assigned to the company. For more information about capacity reservation rules, see [Capacity and Reservations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/capacity-management.md).
-   If the tasks assigned to the outsourced service provider is more than its defined capacity, a red vertical bar displays on the calendar, indicating over-allocation of tasks.

