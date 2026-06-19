---
title: Structured workflows for Exercises
description: Manage exercises using structured workflows in the Business Continuity Workspace \(also known as BCM Configurable Workspace\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/performing-tasks-to-manage-exercise-events.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Structured workflows for Exercises

Manage exercises using structured workflows in the Business Continuity Workspace \(also known as BCM Configurable Workspace\).

Business Continuity Management \(BCM\) program managers initiate exercises by defining the scope and severity. They attach important assets, impacted services, and applicable continuity plans to the event, then create and submit tasks to response teams for timely resolution.

-   For more information on creating an exercise, see [Create an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/start-exercise-event-in-uib-ws.md).
-   For more information on adding assets and plans to the exercise, see [Track impacted assets and add associated plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-asset-and-plan-to-exercise-event-uib-ws.md).
-   For more information on adding an event task to the exercise, see [Monitor event tasks and create ad-hoc tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-an-event-task-to-exercise-event.md).
-   For more information on submitting the event task for the exercise event, see [Request an approval and approve the event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/submit-an-event-task-uib-ws.md).
-   You can add event tasks in bulk by applying task template groups or individual task templates from the **Event tasks** tab. For details, see [Monitor event tasks and create ad-hoc tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-an-event-task-to-exercise-event.md) and [Event task creation progress in exercise and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-event-task-template-progress.md).

## Bulk editing of tasks

Starting with version 6.1.x of the Business Continuity Management application, users who have editing access to the event record can now perform bulk edits on tasks directly from the Event tasks related list. This feature is beneficial for users who manage multiple event tasks simultaneously.

For more information on bulk editing of tasks, see [Structured workflows for Crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/perform-tasks-to-manage-crisis-events.md).

## Export and date visibility

Starting with SR - IRM - Business Continuity Management Core - Australia 2026 M06 version, following capabilities are supported for event tasks:

-   Export to Excel: Export the event task list for offline reporting or bulk editing; supports filtering before export.
-   Show actual dates: Toggle to display Actual start and Actual end columns for plan-vs-actual comparison during exercise review.

For additional information on exercises, see [Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/exercise-management-uib.md) and [Home page view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/home-page-uib-ws.md).

-   **[States for an exercise and crisis event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/states-for-exercise-events.md)**  
This section describes the states of progression for an exercises and crisis event.
-   **[Event assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/event-assets.md)**  
When an event is initiated, event assets are managed by using different recovery management methods.
-   **[Mapping event tasks to phases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/mapping-event-tasks-to-phases.md)**  
Starting with BCM, version 9.x.x, BCM administrators set up active phases in the Core UI for improved event task management. BCM users then map these phases to event tasks and execute them in the set order, ensuring a logical execution sequence. The phases can be deactivated only; they cannot be deleted.
-   **[Using nested plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/creating-nested-plan-in-event.md)**  
Configure a system property to control activated plan levels in an event. The system automatically creates nested plans within an event, reducing the manual effort of adding plans and improving system performance. You can also add dependencies between multiple activated plans by updating the **Dependencies** field in the event tasks.
-   **[Adding dependencies of impacted assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/import-event-dep-updates.md)**  
You can add the dependencies of the impacted assets in the events and exercises based on the source data and relationships in the CMDB, BIAs, and plans.
-   **[Enhancing event task management with Hierarchical view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/managing-enhanced-hierarchical-view-in-event-tasks.md)**  
The Hierarchical view for event tasks has been enhanced with several key features. It now displays dependencies between tasks, and shows color-coded states with planned start and end dates. Dependencies can be updated directly through the Hierarchical view \(Gantt chart\), streamlining event task management.
-   **[Event task creation progress in exercise and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-event-task-template-progress.md)**  
When event tasks are created in bulk from task template groups or task templates, the Event tasks list defers refresh to avoid impacting large events. This topic explains the banner and auto-refresh behavior.
-   **[Create an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/start-exercise-event-in-uib-ws.md)**  
Create an exercise in BCM UIB Workspace. You can then test your business continuity and recovery plans on a planned date and monitor the completion of the event tasks.
-   **[Update the event dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/update-event-dep-manually.md)**  
Update the event dependencies manually by selecting the **Update dependencies** UI action. You can update the dependencies in an active event.
-   **[Track impacted assets and add associated plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-asset-and-plan-to-exercise-event-uib-ws.md)**  
Track the impacted assets and add an associated plan to the exercise. You can then monitor the assets and plans for the exercise in BCM UIB Workspace.
-   **[Creating action items in events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/creating-action-items-in-events.md)**  
Starting with BCM release 9.0.x, crisis managers can create action tasks for recovery members or teams anytime during a crisis event or exercise, as long as the event remains open. Crisis managers can create these tasks on the fly without mapping them to event assets or recovery plans. These action tasks are also not included in the event recovery timeline.
-   **[Creating similar tasks groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/identifying-running-dup-tasks-once.md)**  
In BCM, when the same plan is activated multiple times, it can result in multiple redundant tasks. Starting with BCM release 9.0.x, the **Similar tasks groups** tab in events helps you to eliminate redundant tasks by grouping duplicate tasks from multiple plans for similar scenarios. This functionality streamlines event task management and reduces duplication of efforts.
-   **[Import plans and recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/import-the-automated-task-in-an-exercise.md)**  
Import the business continuity plans and associated recovery tasks in the event. Using automated tasks during an exercise enhances efficiency and reduces response time for users.
-   **[Monitor event tasks and create ad-hoc tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-an-event-task-to-exercise-event.md)**  
Monitor event task completion and create ad-hoc tasks as necessary in the exercise from the BCM Configurable Workspace. The tasks are then completed in a sequence.
-   **[Importing and exporting event tasks in Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-export-import-feature-event-tasks.md)**  
Use Export to download event task records into a structured Microsoft Excel file — complete with dropdowns, instructions, and field protection. Edit records offline, then use Import to upload the updated file and apply bulk changes.
-   **[Start an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/start-event.md)**  
To initiate an event, first pull the relevant plans into the event, and then review the event tasks listed in the **Event tasks** tab.
-   **[Request an approval and approve the event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/submit-an-event-task-uib-ws.md)**  
Approve the exercise in BCM UIB Workspace.
-   **[View recovery tasks from Self-Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/view-recovery-tasks-from-self-service-uib-ws.md)**  
View the recovery tasks that are assigned to you or the recovery task team to recover assets from a crisis event or exercise. Your BCM program manager assigns the tasks to you and you can view them from the self-service application menu.
-   **[View 360° relationships for exercises and crises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/relationship-view-exercise-crisis.md)**  
Visualize the 360° relationships for an exercise or a crisis event and the associated entities in BCM UIB Workspace. You can access the 360° view at any time while creating an exercise and a crisis event.
-   **[Generate event reports in PDF or Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/generate-pdf-for-events.md)**  
Generate the PDF or Microsoft Word copy of an exercise or a crisis event in the BCM Configurable Workspace and save it for a future reference.

**Parent Topic:**[Managing BCM workflow tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/manage-bcm-with-uib-workspace.md)

