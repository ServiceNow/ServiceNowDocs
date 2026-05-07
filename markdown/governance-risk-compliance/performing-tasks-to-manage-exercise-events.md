---
title: Structured workflows for exercises
description: Manage exercises using structured workflows in the Business Continuity Workspace \(also known as BCM Configurable Workspace\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Structured workflows for exercises

Manage exercises using structured workflows in the Business Continuity Workspace \(also known as BCM Configurable Workspace\).

Business Continuity Management \(BCM\) program managers initiate exercises by defining the scope and severity. They attach important assets, impacted services, and applicable continuity plans to the event, then create and submit tasks to response teams for timely resolution.

-   For more information on creating an exercise, see [Create an exercise](../task/start-exercise-event-in-uib-ws.md).
-   For more information on adding assets and plans to the exercise, see [Track impacted assets and add associated plans](../task/add-asset-and-plan-to-exercise-event-uib-ws.md).
-   For more information on adding an event task to the exercise, see [Monitor event tasks and create ad-hoc tasks](../task/add-an-event-task-to-exercise-event.md).
-   For more information on submitting the event task for the exercise event, see [Request an approval and approve the event](../task/submit-an-event-task-uib-ws.md).

## Bulk editing of tasks

Starting with version 6.1.x of the Business Continuity Management application, users who have editing access to the event record can now perform bulk edits on tasks directly from the Event tasks related list. This feature is beneficial for users who manage multiple event tasks simultaneously.

For more information on bulk editing of tasks, see [Structured workflows for crisis events](perform-tasks-to-manage-crisis-events.md).

For additional information on exercises, see [Exercises](exercise-management-uib.md) and [Home page view](home-page-uib-ws.md).

-   **[States for an exercise and crisis event](states-for-exercise-events.md)**  
This section describes the states of progression for an exercises and crisis event.
-   **[Event assets](event-assets.md)**  
When an event is initiated, event assets are managed by using different recovery management methods.
-   **[Mapping event tasks to phases](mapping-event-tasks-to-phases.md)**  
Starting with BCM, version 9.x.x, BCM administrators set up active phases in the Core UI for improved event task management. BCM users then map these phases to event tasks and execute them in the set order, ensuring a logical execution sequence. The phases can be deactivated only; they cannot be deleted.
-   **[Using nested plans](creating-nested-plan-in-event.md)**  
Configure a system property to control activated plan levels in an event. The system automatically creates nested plans within an event, reducing the manual effort of adding plans and improving system performance. You can also add dependencies between multiple activated plans by updating the **Dependencies** field in the event tasks.
-   **[Adding dependencies of impacted assets](import-event-dep-updates.md)**  
You can add the dependencies of the impacted assets in the events and exercises based on the source data and relationships in the CMDB, BIAs, and plans.
-   **[Enhancing event task management with Hierarchical view](managing-enhanced-hierarchical-view-in-event-tasks.md)**  
The Hierarchical view for event tasks has been enhanced with several key features. It now displays dependencies between tasks, and shows color-coded states with planned start and end dates. Dependencies can be updated directly through the Hierarchical view \(Gantt chart\), streamlining event task management.
-   **[Create an exercise](../task/start-exercise-event-in-uib-ws.md)**  
Create an exercise in BCM UIB Workspace. You can then test your business continuity and recovery plans on a planned date and monitor the completion of the event tasks.
-   **[Update the event dependencies](../task/update-event-dep-manually.md)**  
Update the event dependencies manually by selecting the **Update dependencies** UI action. You can update the dependencies in an active event.
-   **[Track impacted assets and add associated plans](../task/add-asset-and-plan-to-exercise-event-uib-ws.md)**  
Track the impacted assets and add an associated plan to the exercise. You can then monitor the assets and plans for the exercise in BCM UIB Workspace.
-   **[Creating action items in events](creating-action-items-in-events.md)**  
Starting with BCM release 9.0.x, crisis managers can create action tasks for recovery members or teams anytime during a crisis event or exercise, as long as the event remains open. Crisis managers can create these tasks on the fly without mapping them to event assets or recovery plans. These action tasks are also not included in the event recovery timeline.
-   **[Creating similar tasks groups](identifying-running-dup-tasks-once.md)**  
In BCM, when the same plan is activated multiple times, it can result in multiple redundant tasks. Starting with BCM release 9.0.x, the **Similar tasks groups** tab in events helps you to eliminate redundant tasks by grouping duplicate tasks from multiple plans for similar scenarios. This functionality streamlines event task management and reduces duplication of efforts.
-   **[Import plans and recovery tasks](../task/import-the-automated-task-in-an-exercise.md)**  
Import the business continuity plans and associated recovery tasks in the event. Using automated tasks during an exercise enhances efficiency and reduces response time for users.
-   **[Monitor event tasks and create ad-hoc tasks](../task/add-an-event-task-to-exercise-event.md)**  
Monitor event task completion and create ad-hoc tasks as necessary in the exercise from the BCM Configurable Workspace. The tasks are then completed in a sequence.
-   **[Start an event](../task/start-event.md)**  
To initiate an event, first pull the relevant plans into the event, and then review the event tasks listed in the **Event tasks** tab.
-   **[Request an approval and approve the event](../task/submit-an-event-task-uib-ws.md)**  
Approve the exercise in BCM UIB Workspace.
-   **[View recovery tasks from Self-Service](../task/view-recovery-tasks-from-self-service-uib-ws.md)**  
View the recovery tasks that are assigned to you or the recovery task team to recover assets from a crisis event or exercise. Your BCM program manager assigns the tasks to you and you can view them from the self-service application menu.
-   **[View 360° relationships for exercises and crises](../task/relationship-view-exercise-crisis.md)**  
Visualize the 360° relationships for an exercise or a crisis event and the associated entities in BCM UIB Workspace. You can access the 360° view at any time while creating an exercise and a crisis event.
-   **[Generate event reports in PDF or Microsoft Word](../task/generate-pdf-for-events.md)**  
Generate the PDF or Microsoft Word copy of an exercise or a crisis event in the BCM Configurable Workspace and save it for a future reference.

**Parent Topic:**[Managing BCM workflow tasks](manage-bcm-with-uib-workspace.md)

