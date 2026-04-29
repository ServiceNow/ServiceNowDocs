---
title: Structured workflows for BCPs
description: Perform the structured workflows that are outlined in this section to create a business continuity plan in Business Continuity Workspace \(also known as BCM Configurable Workspace\).
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Structured workflows for BCPs

Perform the structured workflows that are outlined in this section to create a business continuity plan in Business Continuity Workspace \(also known as BCM Configurable Workspace\).

Business continuity plan owner creates a business continuity plan as per the plan template, adds an asset and scope to the plan, creates documentation sections, adds the related plan and recovery team, adds a loss scenario with recovery strategy and recovery task, and generates and saves the PDF of the analysis for reference.

-   For information on creating a business continuity plan, see [Create a business continuity plan](../task/create-bcp-plan-in-uib-ws.md). For information on adding an asset and scope to the plan, see [Add asset and scope to the BCP](../task/add-asset-plan-scope-for-bcp-uib-ws.md).
-   For information on creating a documentation section, see [Create documentation sections](../task/create-documentation-section-bcp.md). For information on adding the related plan and recovery team, see [Add associated plans and recovery teams](../task/add-related-plans-recovery-teams-bcp-uib-ws.md).
-   For information on adding a loss scenario, recovery strategy, and recovery task, see [Add loss scenarios](../task/add-loss-scenario-recovery-task-bcp-uib-ws.md), [Add recovery strategies for dependencies](../task/create-new-recovery-strategy-for-loss-scenario-uib-ws.md), and [Add recovery tasks](../task/add-a-recovery-task.md).
-   For information on generating and saving the PDF, see [Generate BCP reports in PDF or Microsoft Word format](../task/generate-pdf-for-bcp.md).

## Hierarchical plan structure enhancement

Starting with BCM, version 9.x.x, the hierarchical structure of parent-child plans verifies logical organization and execution of recovery tasks. With this enhancement, when an event is triggered, only relevant child plans are brought into the scope, allowing plan execution and dependencies to cascade downward in a controlled manner.

Parent plans are excluded to prevent the inclusion of unrelated scenarios that may require subsequent cancellation. This approach confirms that only relevant plans are considered, maintaining a focused and efficient recovery process.

The system also performs cyclic dependency checks automatically, ensuring that the hierarchy always flows one directionally—from parent plans to child plans.

Implementing the hierarchical plan structure offers these key benefits:

-   Logical task execution: Only after the necessary tasks in the parent plans have been completed, tasks in the child plans are executed, ensuring a controlled and sequential recovery process.
-   Avoidance of circular dependencies: The system is designed to prevent circular dependencies, maintaining a unidirectional flow from parent to child plans and avoiding potential conflicts.
-   Parallel execution: Tasks within the same plan can be executed in parallel when possible, optimizing recovery time and efficiency.

By introducing this hierarchical structure, the system provides an organized and manageable approach to plan management, enhancing efficiency and effectiveness in disaster recovery planning and execution.

## Nested related plans

Beginning with the Xanadu release, the handling of nested related plans has improved. This enhancement helps in managing potential cyclic dependencies by detecting and highlighting any problems that could cause cyclic dependencies during the execution of tasks.

Additionally, the refined recovery timelines enable you to monitor the planned and actual timeframes. A task may be applied to all assets within a plan or to none at all, facilitating an accurate aggregation of recovery timeframes across various levels, including assets, tasks, and plans.

## Additional information on Business Continuity Planning

-   For information on the **Planning** tab in the Home page, see [Home page view](home-page-uib-ws.md).
-   For information on business continuity planning, see [Business continuity planning](bcp-uib.md).
-   For information on the administrative tasks in business continuity planning, see [Setup for a business continuity plan](bcp-admin-tasks.md).

-   **[States and UI actions for a BCP](states-ui-actions-bcp.md)**  
When you create a business continuity plan \(BCP\), certain UI actions are associated with each state.
-   **[Create a business continuity plan](../task/create-bcp-plan-in-uib-ws.md)**  
Create a business continuity plan in BCM UIB Workspace.
-   **[Scheduling auto-update of related assets](import-cmdb-updates-in-plans.md)**  
You can schedule an auto-update of the related assets in the plans based on the source data and relationships in the CMDB. You can receive an email notification with details of the plan dependency updates from the BCM application. Dependencies are fetched from different sources such as BIA upstream dependency, BIA downstream dependencies, and CMDB.
-   **[Add asset and scope to the BCP](../task/add-asset-plan-scope-for-bcp-uib-ws.md)**  
Add an asset and the scope to the business continuity plan \(BCP\). You can then view the primary elements in the BCM Configurable Workspace.
-   **[Create documentation sections](../task/create-documentation-section-bcp.md)**  
Create a documentation section in the business continuity plan. You can then document the recovery capabilities of your business continuity plan in BCM UIB Workspace.
-   **[Add associated plans and recovery teams](../task/add-related-plans-recovery-teams-bcp-uib-ws.md)**  
Add your business continuity associated plans and recovery teams to your business continuity plan. You can then view the details in BCM UIB Workspace.
-   **[Add loss scenarios](../task/add-loss-scenario-recovery-task-bcp-uib-ws.md)**  
Add a loss scenario and define the related asset dependencies in your business continuity plan. You can then view the details of the assets in BCM UIB Workspace and then plan a recovery strategy for an identified loss scenario.
-   **[Add recovery strategies for dependencies](../task/create-new-recovery-strategy-for-loss-scenario-uib-ws.md)**  
Add a recovery strategy for the related asset dependencies and estimate the time to implement the strategy. You can then get the assets up and running quickly in an identified loss scenario.
-   **[Mapping recovery tasks to phases](mapping-recovery-tasks-to-phases.md)**  
Starting with BCM, version 9.x.x, BCM administrators set up active phases for plans and events, enhancing recovery and event task management. BCM managers then map these phases to recovery and event tasks, executing them in a desired, logical sequence.
-   **[Add recovery tasks](../task/add-a-recovery-task.md)**  
Add a recovery task as part of the planned recovery strategy. You can add one or more recovery tasks for a loss scenario and those recovery tasks are displayed in the loss scenario itself. Automate the recovery tasks in a plan for a faster recovery.
-   **[Automate recovery tasks](../task/automate-the-recovery-tasks.md)**  
Automate the manual recovery task within the business continuity plan. You can classify the manual recovery task as an automated task first and then attach an automated flow to it.
-   **[Submit the BCP for approval](../task/submit-bcp-for-review.md)**  
Submit the business continuity plan \(BCP\) for an approval. You can then view the details in BCM UIB Workspace.
-   **[Visualize 360° relationships for the BCP](../task/relationship-view-bcp.md)**  
Visualize the 360° relationships for a business continuity plan \(BCP\) and its associated entities in BCM UIB Workspace. You can access the 360° view at any time while working on the business continuity plan.
-   **[Generate BCP reports in PDF or Microsoft Word format](../task/generate-pdf-for-bcp.md)**  
Generate a PDF or Microsoft Word copy of a business continuity plan in the BCM Configurable Workspace and save it for a future reference.

**Parent Topic:**[Managing BCM workflow tasks](manage-bcm-with-uib-workspace.md)

