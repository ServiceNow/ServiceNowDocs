---
title: Assign work order tasks to crews on Dispatcher Workspace
description: Assign crews to a work order task that requires a crew of agents in Dispatcher Workspace.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Using Dispatcher Workspace for crew operations, Using Dispatcher Workspace, Assigning work order tasks to agents from Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Assign work order tasks to crews on Dispatcher Workspace

Assign crews to a work order task that requires a crew of agents in Dispatcher Workspace.

## Before you begin

If you’re scheduling a task across multiple schedule entries or days, a work schedule must have been assigned to the crew. For more information, see [Create a work schedule for agents](../../customer-service-management/task/create-agent-work-schedule.md).

**Note:** If the crew schedule hasn’t been defined and you’re auto-assigning a task, the default schedule is used.

If you want to assign work order tasks to crews in the territories that best match their location, you must enable the following options:

-   The Field Service territory model, **Field\_Service\_Territories**. For more information, see [Enable the Field Service territory model](enable-territory-model.md).
-   The **Territory** option in Dispatcher Workspace must be enabled to view the territory information in the task card and the agent card. For more information, see [Enable Dispatcher Workspace settings](dispatcher-wrkspc-settings.md).

Role required: wm\_dispatcher

## About this task

You can assign tasks that are in the Pending Dispatch state. When assigning and dispatching work order tasks to crews, consider the following aspects:

-   Task completion factors: Time required for task completion and task deadlines \(window start and end dates\).
-   Crew assignment considerations: Crew assignment is based on their schedule and availability, ensuring they possess the necessary skill sets and required parts, with availability aligned to configured skill sets. The length of time required to complete a task
-   Agent skills: Aligns specific skills needed for the task with those possessed by crew members.
-   Task requirements: Matches crew capabilities with task demands.

If the Territory Planning plugin is active and Territory Model is enabled, additional factors include:

-   Territorial alignment: Ensures the crew is located within the territory of the task.
-   Territory Membership: Agent eligibility for task assignment is determined by their membership in the associated territory.

Task assignment methods:

1.  Manual Assignment: The dispatcher selects the best crew for the task, ensuring their effective dates align with the task window start and end dates. The dispatcher also checks agent availability within the crew based on their territory membership dates.
2.  Dynamic Assignment: Dynamic Scheduling automatically assigns tasks to crews based on factors like territory alignment, crew availability, agent skills, and task requirements. If a suitable crew exists, it is assigned the task; otherwise, a new crew is created. When the dynamically created crew is assigned for a work order task within a territory, the crew membership is updated and appears in the Crew Membership related list of the territory.

When scheduling tasks for multiple days:

-   View the crew schedule for a selected time period in calendar, such as day, work day, week, two weeks, or four weeks. The calendar also displays the assigned task window spanned across multiple days or weeks.
-   View the recommended crews for the task using the **Auto Assign Rules** option. For more information, see [Search for appropriate Field Service agents](search-agents-tasks.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Search for and open the work order task that you want to assign.

    For more information, see [Search for tasks that need a crew on Dispatcher Workspace](search-crew-task.md).

4.  Select the **Needs Crew** check box if it isn’t already selected.

5.  If you must schedule work order tasks spanning multiple schedule entries or days, select the **Assign across the schedule entries** check box if it isn’t already selected.

6.  Assign the crew task.

<table id="choicetable_tv1_54y_xrb"><thead><tr><th align="left" id="d39893e243">

Option

</th><th align="left" id="d39893e246">

Description

</th></tr></thead><tbody><tr><td id="d39893e252">

**To assign a task manually**

</td><td>

1.  Select a crew task from the task panel.
2.  Drag the task to the calendar slot of a crew that is recommended for a task.
3.  Select **Save**.


</td></tr><tr><td id="d39893e276">

**To manually assign a task from the task panel**

</td><td>

1.  Select the More actions icon \(![More actions icon](../image/more_actions.png)\) for a task that requires a crew in the task panel.
2.  Select the **Assign** field.
3.  Search for and select a crew in the **Assigned crew** field.
4.  Select **Save**.


</td></tr><tr><td id="d39893e315">

**To auto-assign the task to a crew from the task panel**

</td><td>

1.  Select the More actions icon \(![More actions icon](../image/more_actions.png)\) on the crew task card.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d39893e348">

**To auto-assign the task to a crew from the task record**

</td><td>

1.  Select a work order task that requires crew from the task panel.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d39893e376">

**To auto-assign the task to a crew from a list**

</td><td>

1.  Select the Lists icon \( ![List icon.](../image/lists_icon.png)\) and select **My Dispatch Queue**.
2.  Select the work order task.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr><tr><td id="d39893e415">

**To manually assign a task from the contextual side panel**

</td><td>

1.  Select a work order task in the task panel or on the map.
2.  Select the Overflow actions \(![overflow actions](../image/overflow-actions.png)\) icon in the contextual side panel.
3.  Select the **Assign** field.
4.  Search for and select a crew in the **Assigned crew** field.
5.  Select **Save**.


</td></tr><tr><td id="d39893e457">

**To auto-assign the task to a crew from the contextual side panel**

</td><td>

1.  Select a work order task in the task panel or on the map.
2.  Select the Overflow actions \(![overflow actions](../image/overflow-actions.png)\) icon in the contextual side panel.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr></tbody>
</table>7.  Select **Save**.


## Result

The task is assigned to the crew. All crew members receive a push notification that the work order task is assigned. The Task Assignees related list is added to the work order task. The list displays the names of crew members, which include both the leader of the crew and the agents in the crew.

**Parent Topic:**[Using Dispatcher Workspace for crew operations](../concept/using-disp-wrkspc-crew-operations.md)

