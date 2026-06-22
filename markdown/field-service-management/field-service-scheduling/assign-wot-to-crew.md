---
title: Assign work order tasks to crews on Dispatcher Workspace
description: Assign crews to a work order task that requires a crew of agents in Dispatcher Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/assign-wot-to-crew.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Crew operations, Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Assign work order tasks to crews on Dispatcher Workspace

Assign crews to a work order task that requires a crew of agents in Dispatcher Workspace.

## Before you begin

If you’re scheduling a task across multiple schedule entries or days, a work schedule must have been assigned to the crew. For more information, see [Create a work schedule for agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-manager-workforce/create-agent-work-schedule.md).

**Note:** If the crew schedule hasn’t been defined and you’re auto-assigning a task, the default schedule is used.

If you want to assign work order tasks to crews in the territories that best match their location, you must enable the following options:

-   The Field Service territory model, **Field\_Service\_Territories**. For more information, see [Enable the Field Service territory model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/enable-territory-model.md).
-   The **Territory** option in Dispatcher Workspace must be enabled to view the territory information in the task card and the agent card. For more information, see [Enable Dispatcher Workspace settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/dispatcher-wrkspc-settings.md).

Role required: wm\_dispatcher

## About this task

You can assign tasks that are in the Pending Dispatch state. When assigning and dispatching work order tasks to crews, consider the following aspects:

-   Task completion factors: Time required for task completion and task deadlines \(window start and end dates\).
-   Crew assignment considerations: Crew assignment is based on their schedule and availability, ensuring they possess the necessary skill sets and required parts, with availability aligned to configured skill sets. The length of time required to complete a task
-   Agent skills: Aligns specific skills needed for the task with those possessed by crew members.
-   Task requirements: Matches crew capabilities with task demands.

If the Territory Planning plugin is active and Territory Model is enabled, additional factors include:

-   Territorial alignment: Ensures that the crew is located within the territory of the task.
-   Territory Membership: Agent eligibility for task assignment is determined by their membership in the associated territory.

Task assignment methods:

1.  Manual Assignment: The dispatcher selects the best crew for the task, verifying their effective dates align with the task window start and end dates. The dispatcher also checks agent availability within the crew based on their territory membership dates.
2.  Dynamic Assignment: Dynamic Scheduling automatically assigns tasks to crews based on factors like territory alignment, crew availability, agent skills, and task requirements. If a suitable crew exists, it’s assigned the task. Otherwise, a new crew is created. When the dynamically created crew is assigned for a work order task within a territory, the crew membership is updated and appears in the Crew Membership related list of the territory.

When scheduling tasks for multiple days:

-   View the crew schedule for a selected time period in the calendar, such as day, work day, week, two weeks, or four weeks. The calendar also displays the assigned task window spanned across multiple days or weeks.
-   View the recommended crews for the task using the **Auto Assign Rules** option. For more information, see [Search for appropriate Field Service agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/search-agents-tasks.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Search for and open the work order task that you want to assign.

    For more information, see [Search for tasks that need a crew on Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/search-crew-task.md).

4.  Select the **Needs Crew** check box if it isn’t already selected.

5.  If you must schedule work order tasks spanning multiple schedule entries or days, select the **Assign across the schedule entries** check box if it isn’t already selected.

6.  Assign the crew task.

<table id="choicetable_tv1_54y_xrb"><thead><tr><th align="left" id="d38944e254">

Option

</th><th align="left" id="d38944e257">

Description

</th></tr></thead><tbody><tr><td id="d38944e263">

**To assign a task manually**

</td><td>

1.  Select a crew task from the task panel.
2.  Drag the task to the calendar slot of a crew that is recommended for a task.
3.  Select **Save**.


</td></tr><tr><td id="d38944e287">

**To manually assign a task from the task panel**

</td><td>

1.  Select the More actions icon \(\[Omitted image "more\_actions.png"\] Alt text: More actions icon\) for a task that requires a crew in the task panel.
2.  Select the **Assign** field.
3.  Search for and select a crew in the **Assigned crew** field.
4.  Select **Save**.


</td></tr><tr><td id="d38944e326">

**To auto-assign the task to a crew from the task panel**

</td><td>

1.  Select the More actions icon \(\[Omitted image "more\_actions.png"\] Alt text: More actions icon\) on the crew task card.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d38944e359">

**To auto-assign the task to a crew from the task record**

</td><td>

1.  Select a work order task that requires crew from the task panel.
2.  Select **Auto Assign**.
3.  Select **Confirm**.


</td></tr><tr><td id="d38944e387">

**To auto-assign the task to a crew from a list**

</td><td>

1.  Select the Lists icon \( \[Omitted image "lists\_icon.png"\] Alt text: List icon.\) and select **My Dispatch Queue**.
2.  Select the work order task.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr><tr><td id="d38944e426">

**To manually assign a task from the contextual side panel**

</td><td>

1.  Select a work order task in the task panel or on the map.
2.  Select the Overflow actions \(\[Omitted image "overflow-actions.png"\] Alt text: overflow actions\) icon in the contextual side panel.
3.  Select the **Assign** field.
4.  Search for and select a crew in the **Assigned crew** field.
5.  Select **Save**.


</td></tr><tr><td id="d38944e468">

**To auto-assign the task to a crew from the contextual side panel**

</td><td>

1.  Select a work order task in the task panel or on the map.
2.  Select the Overflow actions \(\[Omitted image "overflow-actions.png"\] Alt text: overflow actions\) icon in the contextual side panel.
3.  Select **Auto Assign**.
4.  Select **Confirm**.


</td></tr></tbody>
</table>7.  Select **Save**.


## Result

The task is assigned to the crew. All crew members receive a push notification that the work order task is assigned. The Task Assignees related list is added to the work order task. The list displays the names of crew members, which include both the leader of the crew and the agents in the crew.

