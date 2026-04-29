---
title: Assigning work order tasks to agents manually
description: When all of the work order tasks associated with a work order are qualified, you can dispatch the work order tasks. You can dispatch them from either the task form, the task map, or Dispatcher Workspace.Dispatch a work order task from the dispatch queue. You can also reassign the task from the queue.Dispatch a work order task from the task map. You can also reassign the task from the map.Automatically match a task to a nearby agent who has the necessary skills and a schedule that can accommodate the task.Request more details from the qualifier if there is not enough information in the task record to dispatch a work order task.Quickly sort a list of the best agents to assign a work order task based on the criteria that you choose from. This feature works the same way as using assignment assistance in Dispatcher Workspace.You can flag a task from the work order task page. This makes it easier to follow up on work order tasks that might need attention later.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Scheduling and dispatching, Use, Field Service Management]
---

# Assigning work order tasks to agents manually

When all of the work order tasks associated with a work order are qualified, you can dispatch the work order tasks. You can dispatch them from either the task form, the task map, or Dispatcher Workspace.

When all of the associated work order tasks are qualified, the state of the parent work order changes to Qualified. If you have already [sourced parts](c_SourceParts.md) and created [transfer order lines](../task/create-transfer-order.md), then you are ready to begin dispatching the work order tasks to agents.

Users with the following roles can dispatch work order tasks: wm\_dispatcher, wm\_initiator\_qualifier\_dispatcher, or wm\_admin.

You can dispatch work order tasks to qualified work agents from these locations:

-   [Dispatch queue](c_DispatchWorkOrderTasks.md#): Dispatch tasks to agents from task records.
-   [Task map](c_DispatchWorkOrderTasks.md#): Dispatch tasks to agents using a Google map with geolocation.
-   Dispatcher Workspace: Dispatch tasks to agents using the drag-and-drop and auto-assign capabilities.

**Note:** When dynamic scheduling is enabled, dispatchers can manually double-book an agent for more than one work order task with overlapping time. You can enable double booking using **work.management.allow.doublebooking.dynamicscheduling** [system property](../reference/r_InstalledWithFSM.md).

## Assign work order tasks to agents or crews from the dispatch queue

Dispatch a work order task from the dispatch queue. You can also reassign the task from the queue.

### Before you begin

Role required: wm\_dispatcher, wm\_initiator\_qualifier\_dispatcher, or wm\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **My Dispatch Queue**.

2.  Open a work order task.

3.  Assign task to an agent or a crew.

<table id="choicetable_rqt_352_vtb"><thead><tr><th align="left" id="d91403e236">

Option

</th><th align="left" id="d91403e239">

Description

</th></tr></thead><tbody><tr><td id="d91403e245">

**If Territory Planning is not enabled**

</td><td>

1.  Select an **Assignment group**.
2.  Set the **Assigned to** field to an agent who is close to the task location.

**Note:** If the **Needs crew** option is selected, then this field name changes to Assigned crew and you can assign the task to a crew that is close to the task location.

A warning message appears if the assigned task is outside the radius between the task location and the agent's location.

</td></tr><tr><td id="d91403e277">

**If Territory Planning is enabled**

</td><td>

1.  Select a **Territory**.
2.  Select an **Dispatch group**.
3.  Select an **Assignment group**.
4.  Set the **Assigned to** field to an agent who is close to the task location.

**Note:** If the **Needs crew** option is selected, then this field name changes to Assigned crew and you can assign the task to a crew that is close to the task location.

A warning message appears if the assigned task is outside the radius between the task location and the agent's location.

</td></tr></tbody>
</table>4.  Click **Update**.


### Result

The work order task is assigned to the selected agent or a crew.

If the agent rejects the task, you can view the task rejection details in the Task Rejections related list of the work order task. If the agent does not accept in a specific time period, the work order task is automatically rejected. You can reassign the task to another available agents.

## Dispatch a work order task from the task map

Dispatch a work order task from the task map. You can also reassign the task from the map.

### Before you begin

Role required: wm\_dispatcher, wm\_initiator\_qualifier\_dispatcher, or wm\_admin

### About this task

You can use the dispatch map if you urgently need to dispatch a task or to reassign a task to an alternative agent. The task must have a location with a defined latitude and longitude.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **My Dispatch Queue**.

2.  Open the work order task that you want to dispatch or reassign.

3.  Click **View Task on Map**.

    This button is available only if the task contains a location with a defined latitude and longitude. The map displays a red task icon with a black spot for the task, and shows icons for all nearby agents.

    ![view task on map button](../../field-service-management/image/task-map.png)

4.  To apply filters on the agents, do the following:

    1.  Click **View Filter**.

    2.  Select a skill level for the agents to display in the map.

        Possible filters for skills are as follows:

        -   **Match all needed skills**
        -   **Match some needed skills**
        -   **Match none of skills**
    3.  Click **Apply Filter**.

    The list shows the agents on the map who match the skills selection.

5.  Click an agent icon to show the agent's name, skills, and schedule.

6.  Click the icon![paper with a plus sign on top of it](../../field-service-management/image/WM_Assign_Task_icon.png) beside the agent's name to assign the task to that agent.


### Result

If the task can fit within the agent's schedule, the task is assigned to the agent and a confirmation message is displayed.

If the agent's schedule cannot accommodate the task, the system displays a failure message and enables you to select a different agent.

## Auto-dispatch a work order task

Automatically match a task to a nearby agent who has the necessary skills and a schedule that can accommodate the task.

### Before you begin

Role required: wm\_dispatcher, wm\_initiator\_qualifier\_dispatcher, or wm\_admin

### About this task

Auto-dispatch evaluates an agent's dispatch group, assignment group, location, or skills before assigning a task. If the Territory Planning feature is enabled, then auto-dispatch identifies the list of dispatch groups to select from based on the selected territory before assigning the task to an agent or a crew.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **My Dispatch Queue**.

2.  Open a task.

3.  If you need to assign the task to a crew, select the **Needs Crew** check box if it is not already selected.

4.  If Field Service Territory Planning is enabled, perform the following steps.

    1.  Select a **Territory**.

        The list of best matched territories are filtered based on the location of the work order task.

    2.  Select a **Dispatch group**.

        The list displays the dispatch groups that are associated with the selected territory.

5.  Click **Auto-Dispatch**.


### Result

The system assigns the work order task to an agent or a crew who is close to the task location. Closeness is measured based on either the**Distance from task with radius exclusion** task filter or the **Radius exclusion** task filter.

If the system cannot find an appropriate agent, a failure message is displayed. The task stays in the Pending Dispatch state.

If the agent does not accept in a specific time period, the work order task is automatically rejected. The dispatcher can reassign the task to other available agents.

## Request additional information from a work order task

Request more details from the qualifier if there is not enough information in the task record to dispatch a work order task.

### Before you begin

Role required: wm\_dispatcher, wm\_initiator\_qualifier\_dispatcher, or wm\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatch Queue**.

2.  Open a work order task in Pending Dispatch state.

3.  In the **Work Notes** field, enter a reason for returning the work order task.

4.  Click **Request more information**.


### Result

The work order task is moved to the Draft state.

The work order is moved to the Awaiting Qualification state. If Field Service Management is configured for automatic qualification, the work order state remains at **Qualified**.

## Suggest agents to assign to a work order task from the work order task page

Quickly sort a list of the best agents to assign a work order task based on the criteria that you choose from. This feature works the same way as using assignment assistance in Dispatcher Workspace.

### Before you begin

Role required: wm\_dispatcher

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **My Dispatch Queue**.

2.  Select the work order task that you want to assign an agent to.

3.  Select **Assignment assistance**.

    ![assignment assistance on records page](../../field-service-management/image/assign-assistance-task.png)

4.  Sort the agent list based on the criteria that you want.

    |Sort option|Description|
    |-----------|-----------|
    |Best Match|Best match is the default sorting method. Match percentage is calculated the same way that Dynamic Scheduling calculates agents to assign tasks to. For more information, see [Matching criteria for assigning tasks](../../field-service-management/task/create-dynamic-scheduling-config.md#).|
    |Distance|Sorts agents based on how far each agent is from the work order task.|
    |Skills|Sorts agents based on the number of required skills that each agent has. Agents with more skills are at the top.|
    |Parts|Sorts agents based on how many required parts each agent has. Agents with the most parts to complete the task are at the top.|
    |Earliest start time|Sorts agents based on how quickly they can start the work order task.|
    |Earliest end time|Sorts agents based on how quickly they can complete the work order task.|

5.  Select the agent to whom you want to assign the work order task.

6.  Select **Save**.


## Flag a work order task

You can flag a task from the work order task page. This makes it easier to follow up on work order tasks that might need attention later.

### About this task

This feature works the same way as the Flag a task function that shows on the task card in Dispatcher Workspace.

### Before you begin

Role required: wm\_dispatcher

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **My Dispatch Queue**.

2.  Select the work order task that you want to flag.

3.  Select **Flag Task**.

    ![flag task button on records page](../../field-service-management/image/select-flag-task.png)

    The work order task is flagged and can be found under **All** &gt; **Field Service** &gt; **Work Order** &gt; **My Flagged Tasks**.


