---
title: Structured workflows for BCPs
description: Perform the structured workflows that are outlined in this section to create a business continuity plan in Business Continuity Workspace \(also known as BCM Configurable Workspace\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Structured workflows for BCPs

Perform the structured workflows that are outlined in this section to create a business continuity plan in Business Continuity Workspace \(also known as BCM Configurable Workspace\).

Business continuity plan owner creates a business continuity plan as per the plan template, adds an asset and scope to the plan, creates documentation sections, adds the related plan and recovery team, adds a loss scenario with recovery strategy and recovery task, and generates and saves the PDF of the analysis for reference.

-   For information on creating a business continuity plan, see [Create a business continuity plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-bcp-plan-in-uib-ws.md). For information on adding an asset and scope to the plan, see [Add asset and scope to the BCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-asset-plan-scope-for-bcp-uib-ws.md).
-   For information on creating a documentation section, see [Create documentation sections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-documentation-section-bcp.md). For information on adding the related plan and recovery team, see [Add associated plans and recovery teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-related-plans-recovery-teams-bcp-uib-ws.md).
-   For information on adding a loss scenario, recovery strategy, and recovery task, see [Add loss scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-loss-scenario-recovery-task-bcp-uib-ws.md), [Add recovery strategies for dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-recovery-strategy-for-loss-scenario-uib-ws.md), and [Add recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-a-recovery-task.md).
-   For information on generating and saving the PDF, see [Generate BCP reports in PDF or Microsoft Word format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/generate-pdf-for-bcp.md).

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

-   For information on the **Planning** tab in the Home page, see [Home page view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/home-page-uib-ws.md).
-   For information on business continuity planning, see [Business continuity planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-uib.md).
-   For information on the administrative tasks in business continuity planning, see [Setup for a business continuity plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-admin-tasks.md).

-   **[States and UI actions for a BCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/states-ui-actions-bcp.md)**  
When you create a business continuity plan \(BCP\), certain UI actions are associated with each state.
-   **[Recovery strategy and task templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/recovery-strategy-and-task-templates-overview.md)**  
Business continuity planners often rebuild the same recovery structures each time they author a plan. Reusable templates remove that repetition by capturing standard strategies, tasks, and task groupings once and applying them wherever they are needed.
-   **[Create a business continuity plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-bcp-plan-in-uib-ws.md)**  
Create a business continuity plan in BCM UIB Workspace.
-   **[Create a business continuity plan from a plan template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-bcp-plan-from-template-in-uib-ws.md)**  
Create a business continuity plan from a plan template in BCM UIB Workspace so that the loss scenarios, recovery strategies, and recovery tasks defined on the template are generated automatically.
-   **[Scheduling auto-update of related assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/import-cmdb-updates-in-plans.md)**  
You can schedule an auto-update of the related assets in the plans based on the source data and relationships in the CMDB. You can receive an email notification with details of the plan dependency updates from the BCM application. Dependencies are fetched from different sources such as BIA upstream dependency, BIA downstream dependencies, and CMDB.
-   **[Add asset and scope to the BCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-asset-plan-scope-for-bcp-uib-ws.md)**  
Add an asset and the scope to the business continuity plan \(BCP\). You can then view the primary elements in the BCM Configurable Workspace.
-   **[Create documentation sections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-documentation-section-bcp.md)**  
Create a documentation section in the business continuity plan. You can then document the recovery capabilities of your business continuity plan in BCM UIB Workspace.
-   **[Add associated plans and recovery teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-related-plans-recovery-teams-bcp-uib-ws.md)**  
Add your business continuity associated plans and recovery teams to your business continuity plan. You can then view the details in BCM UIB Workspace.
-   **[Add loss scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-loss-scenario-recovery-task-bcp-uib-ws.md)**  
Add a loss scenario and define the related asset dependencies in your business continuity plan. You can then view the details of the assets in BCM UIB Workspace and then plan a recovery strategy for an identified loss scenario.
-   **[Add recovery strategies for dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-recovery-strategy-for-loss-scenario-uib-ws.md)**  
Add a recovery strategy for the related asset dependencies and estimate the time to implement the strategy. You can then get the assets up and running quickly in an identified loss scenario.
-   **[Configure a recovery strategy template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-strategy-template-uib-ws.md)**  
Configure a reusable recovery strategy template so business continuity planners can apply a pre-defined strategy to loss scenarios without re-entering the implementation details each time.
-   **[Mapping recovery tasks to phases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/mapping-recovery-tasks-to-phases.md)**  
Starting with BCM, version 9.x.x, BCM administrators set up active phases for plans and events, enhancing recovery and event task management. BCM managers then map these phases to recovery and event tasks, executing them in a desired, logical sequence.
-   **[Add recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-a-recovery-task.md)**  
Add a recovery task as part of the planned recovery strategy. You can add one or more recovery tasks for a loss scenario and those recovery tasks are displayed in the loss scenario itself. Automate the recovery tasks in a plan for a faster recovery.
-   **[Apply Task templates and Task template groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reco-task-tem-groups.md)**  
Save individual tasks or groups of tasks for reuse across plans. You can add templates to new plans or inserted into existing ones. You can also generate templates directly from tasks and plans that already exist in the system.
-   **[Create a quick recovery task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-quick-recovery-task.md)**  
Create a quick recovery task from Recovery tasks or as part of the planned recovery strategy for a business continuity plan. Using the quick insert feature, you can create tasks without navigating to a separate form. Tasks can be ordered, inserted in sequence \(before, after, or in parallel with existing tasks\), and dependencies are updated automatically.
-   **[Visualize recovery tasks on Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/view-gantt-chart-for-reco-tasks.md)**  
Use the Gantt chart component on recovery task pages to provide a visual timeline view of tasks associated with the current plan. Customize the view by adding, removing, or reordering columns as needed. The chart is implemented as a UI page to enable customizations and to support multiple versions without requiring changes to existing page behavior.
-   **[Synchronize assets between loss scenarios and recovery strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/syn-ast-be-lo-sce-and-rec-stgy.md)**  
Use the asset syncing fields in the plan template to configure whether assets synchronize to loss scenarios, to recovery strategies, or both. Syncing is a two-step process: assets flow from the plan to loss scenarios first, and then from loss scenarios to recovery strategies.
-   **[Automate recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/automate-the-recovery-tasks.md)**  
Automate the manual recovery task within the business continuity plan. You can classify the manual recovery task as an automated task first and then attach an automated flow to it.
-   **[Submit the BCP for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/submit-bcp-for-review.md)**  
Submit the business continuity plan \(BCP\) for an approval. You can then view the details in BCM UIB Workspace.
-   **[Visualize 360° relationships for the BCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/relationship-view-bcp.md)**  
Visualize the 360° relationships for a business continuity plan \(BCP\) and its associated entities in BCM UIB Workspace. You can access the 360° view at any time while working on the business continuity plan.
-   **[Generate BCP reports in PDF or Microsoft Word format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/generate-pdf-for-bcp.md)**  
Generate a PDF or Microsoft Word copy of a business continuity plan in the BCM Configurable Workspace and save it for a future reference.

**Parent Topic:**[Managing BCM workflow tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/manage-bcm-with-uib-workspace.md)

