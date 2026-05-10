---
title: Using nested plans
description: Configure a system property to control activated plan levels in an event. The system automatically creates nested plans within an event, reducing the manual effort of adding plans and improving system performance. You can also add dependencies between multiple activated plans by updating the Dependencies field in the event tasks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Using nested plans

Configure a system property to control activated plan levels in an event. The system automatically creates nested plans within an event, reducing the manual effort of adding plans and improving system performance. You can also add dependencies between multiple activated plans by updating the **Dependencies** field in the event tasks.

## Changes in the plans and events

Beginning with the Yokohama release, new changes in the plans and events focus on the planning phase and the creation of related plans.

-   **Associating related plans with recovery tasks**

    You can now associate related plans with recovery tasks, helping you identify and manage plan triggers during recovery.

    A new field, **Is associated to task**, has been added to the Related Plans table. If a related plan is associated with a recovery task, the field is set to True. If it is not associated, the field is set to False.

    ![Field.](../image/bcp-rel-plans-asso-to-task.png)

    **Note:** When a related plan listed in the **Related plans** tab is associated with a recovery task, it is created as a child plan in the event. If not associated with any task, it is created as a related plan but not as a child plan.


## Adding a plan to the event

When a plan is added to an event, its related plans and their entire hierarchy are included. Plans manually added to an event are called primary activated plans. Plans without task associations are called related plans. Plans associated with recovery tasks are called child plans.

![Activated plans.](../image/activated-plans.png)

## Using a hierarchy of the plans

Previously, only the primary plan and its directly related plans were included in an event. With the Yokohama release, you can set the **sn\_recovery.max\_activated\_plan\_levels** property to control the depth of activated plans in events, up to 10 levels.

-   **Resetting the property for activated plan levels**

    You can customize the **sn\_recovery.max\_activated\_plan\_levels** property as shown in the examples to control the levels of activated plans that are created in an event.

    -   Set the property to 1 to create only the plans added manually.
    -   Set the property to 2 to create only the primary plan and its first-level related plans.

## Sample use case for a multi-level plan

You can add a multi-level hierarchical plan to an event. Consider the use case where the system property is configured and a few related plans have recovery tasks associated with them. An event is created where the related plans are added to the event.

The primary plan, Plan 1, has Plan 2 and Plan 3 as related plans. Plan 1 includes three recovery tasks: Task 1, Task 2, and Task 3. Task 2 has Plan 2 as a related plan.

![Plan 1.](../image/plan-1.png)

Similarly, Plan 2 has three recovery tasks: Task 1, Task 2, Task 3. Plan 1 triggers Plan 2, and Plan 2 triggers Plan 4 as shown in the example.

![Plan 2.](../image/plan-1-2-4.png)

Previously, when a primary plan like Plan 1 was included in an event, only the first level of related plans, such as Plan 2 and Plan 3, were added. Deeper levels, like Plan 4, were not included. With the nested plan functionality, plans up to 10 levels deep, including Plan 4, can be added to the hierarchy.

When you create an event and add Plan 1, its related plans, assets, and tasks are automatically included. Selecting the **View progress** button opens the Progress tracker window, showing the progress and status of adding plans, assets, tasks, and related plans, and the steps and status of the background process.

![Progress tracker.](../image/progress-tracker.png)

Once all processes are completed, a message prompts you to refresh the page to see the latest updates. You can close the message and then view the created plans and event tasks.

As shown in the example, Plan 1 is the primary plan. Plan 3 is marked as a related plan of Plan 1 because it is not associated with any recovery task. Plan 2 and Plan 4 are child plans because they are associated with recovery tasks.

![Event with plans.](../image/event-with-plans-event-tasks.png)

Event tasks: Event tasks are shown in the list view by default. Switch to the hierarchical view to display the hierarchy, with primary and related plans at the top level.

![List view.](../image/event-task-rel-list-def-view.png)

The example illustrates the hierarchy of event tasks and plans, with the primary plan \(ACP0010118\) and related plan \(ACP0010119\) at the top level.

-   Plan 1 \(ACP0010118\) has three event tasks. The second event task \(EVNTSK0010321\) triggers Plan 2 \(ACP0010120\), and another event task \(EVNTSK0010324\) triggers Plan 4.
-   Plan 3 \(ACP0010119\) has no related activated plan.
-   Two child plans \(ACP0010120 and ACP0010121\) are shown at child levels.

![Hierarchy view.](../image/hier-view.png)

## Navigating between the list view, hierarchical view, and full page view

While working on event tasks, you can navigate between the list view, hierarchical view, and full page view.

-   **List view**

    Arranges event tasks in a list format, making it easy to read and quickly understand the hierarchy. It helps you to scan and find specific information without sifting through lengthy text.

-   **Hierarchical view**

    Visualizes plan dependencies and the order of event tasks. By default, the system shows only primary and related plans in the list view. Switch to the hierarchical view to see the full plan hierarchy.

    **Note:** You can edit event task and plan information in the list view, but the hierarchical view is read-only.

    The Work-breakdown structure \(WBS\) arranges tasks based on their dependencies. For an activated plan, the WBS order is calculated considering both event task and plan dependencies.


![Hierarchical view.](../image/hierarchical-view.png)

-   **Full page view**

    Allows you to see more tasks at once, providing a comprehensive overview of the plan hierarchy and tasks. You can switch between the list, hierarchical, or full-page views.


To return to the original record, select the **Back to record** button.

## Records per level

-   **UI navigation**

    By default, only 10 plans are shown at the first level. If there are more, select the **Show more** button to display additional records. For example, if there are 100 plans, only 10 are shown initially, and selecting **Show more** loads the next set.


## Configuring cross-plan dependencies

You can configure cross-plan dependencies by updating the **Dependencies** field as shown in the example.

**Note:** You can only add dependencies between first-level activated plans.

![Dependency.](../image/event-task-dependency-field.png)

The example shows an activated plan \(ACP0010119\) that depends on another activated plan \(ACP0010118\). Similarly, an event task \(EVNTSK0010326\) can start only after its dependent task \(EVNTSK0010322\) is completed.

![Hierarchical view.](../image/hierarchical-view.png)

**Note:** An event task from a primary or related plan can be associated as a dependency with an event task from the same or another primary or related plan. An event task from a child plan can only be associated as a dependency within the same child plan.

Whenever any event task is updated, as shown in the example, a message indicates that the event tasks have been updated. Selecting **Refresh** loads the updated data.

You can add task dependencies in primary and related plans, but not in child plans. For an event task in a child plan, dependencies can only be selected from the same child plan. For example, in Plan 4, task 3 \(EVNTSK0010331\) depends on tasks \(EVNTSK0010329 and EVNTSK0010330\) within the same child plan.

![Child plan tasks.](../image/child-plan-tasks.png)

When adding task dependencies in primary and related plans, only tasks from other primary or related plans are available for selection in the **Dependencies** field.

![Dependency.](../image/event-task-dependency-field.png)

## Configuring the property to refresh the event task order

Whenever task dependencies are updated, the event task order is updated. If more than 500 event tasks are affected, the order is calculated asynchronously. The **sn\_recovery.sync\_task\_order\_calculation\_limit** property sets the limit for asynchronous calculation to 500 tasks by default. When the task count exceeds this limit and dependencies are updated, the task order calculation becomes asynchronous, and a **Refresh tasks order** button appears in the event, event task, and activated plan. Selecting this button manually refreshes the event task order.

## Process of creating a nested plan

Previously, related plans were created only for primary activated plans. Starting with the Yokohama release, related activated plans can be created from an event task for all activated plan types. An example of creating a nested plan is shown in the diagram.

![Nested plan.](../image/nested-plan.png)

Follow these steps to create a nested plan:

1.  Create an event.
2.  Add a plan to the event. An activated plan is created with the plan type set as primary.
3.  An event is triggered to create related plans. If the plan has related plans without any task associations and the plan level is less than the default value defined in the property, an activated plan is created with the type set as related plan.
4.  An event is created to generate one or more event assets.
5.  After the assets are created, an event is triggered to create event tasks.
6.  If the event task has a related plan and its level is less than the level defined in the property, an activated plan is created with the type set as child plan.

**Parent Topic:**[Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md)

**Parent Topic:**[Structured workflows for crisis events](perform-tasks-to-manage-crisis-events.md)

