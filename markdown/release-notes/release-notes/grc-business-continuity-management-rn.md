---
title: Business Continuity Management release notes
description: The ServiceNow Business Continuity Management application enables your organization to deliver products and services at an acceptable level during disruptive incidents. Business Continuity Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-18"
reading_time_minutes: 5
---

# Business Continuity Management release notes

The ServiceNow® Business Continuity Management application enables your organization to deliver products and services at an acceptable level during disruptive incidents. Business Continuity Management was enhanced and updated in the Australia release.

## Business Continuity Management highlights for the Australia release

-   Build reusable task templates and groups with dependencies across plans, loss scenarios, and exercises.
-   Auto-generate full plan hierarchies — scenarios, strategies, and tasks — from plan templates.
-   Export event tasks to Microsoft Excel, edit offline, and reimport updated records with validation and progress tracking.
-   Monitor performance through role-based dashboards with key performance indicators and usage insights.

See [Business Continuity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/business-continuity-mangmt-overview.md) for more information.

**Important:** Business Continuity Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Task template groups and Task templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reco-task-tem-groups.md)**

    Create reusable Task templates for recovery and event tasks, and organize them into groups with configurable dependencies. Scope groups to all element definitions or a specific type, and define task sequencing within a group to preserve execution order when applied.

-   **[Task templates and Task template groups integration in plan templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-a-bcp-template-uib-ws.md)**

    Associate Task template groups and Task templates at the plan, loss scenario, and recovery strategy levels within a plan template. Creating a plan from a template automatically generates all linked records at each level, with a progress tracker showing status throughout.

-   **[Task templates and Task template groups support in plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reco-task-tem-groups.md)**

    Add Task template groups and individual Task templates directly from recovery task lists.

-   **[Task templates and Task template groups support in Exercises and Crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-an-event-task-to-exercise-event.md)**

    Add task template groups and individual templates directly from event task lists. Select groups, assign an activated plan when required, and the system creates all tasks with dependencies intact. An auto-refresh banner tracks progress and refreshes the list once after all tasks are created.

-   **[Recovery strategy templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-strategy-template-uib-ws.md)**

    Create reusable recovery strategy templates with standard fields including name, description, estimated time limit, and maximum duration. Apply a template to auto-populate a recovery strategy, reducing manual entry and keeping strategies consistent across plans.

-   **[Gantt chart for recovery tasks in plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/view-gantt-chart-for-reco-tasks.md)**

    Visualize recovery task sequences, durations, and dependencies on an interactive Gantt timeline within the plan record. Toggle between list and Gantt views from the **Recovery tasks** tab. Add or edit tasks using a right-select quick-insert panel, pre-filled with task type and sequencing context.

    Filters, sorting, and selections remain consistent when switching between list and Gantt views. The quick-add panel is also available on loss scenario and recovery strategy records. Access is role-controlled: Planners manage tasks in their own plans; Program Managers have full access across all plans.

-   **[Export and import event tasks in Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-export-import-feature-event-tasks.md)**

    Export recovery event tasks to Microsoft Excel from the Event tasks related list. The workbook includes a data sheet, a read-only Event Details tab, and an Instructions sheet. Non-editable columns are locked. Import the updated file when the event is in the Open or Work in progress state. Track import progress in real time, with a full audit trail available on the Recovery Event form.

-   **[Role-based Performance Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/pa-dashboard-summary.md)**

    Access role-based Performance Analytics dashboards directly from the BCM workspace. Four dashboards are available, each tailored to a functional area: Home \(overall BCM status\), BIA \(impact analysis progress\), BCP \(planning records\), and Event \(recovery exercises and activities\). Each dashboard is permission-controlled and views are displayed relevant to the roles.

-   **[Assessment template version control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-smart-asmt-template.md)**

    Track the template version used at the time of assessment creation on Smart Assessment Engine \(SAE\) templates. Assessors and reviewers can clearly see which template version was in effect, making it easier to audit and compare assessments over time.


## UI changes

-   **[Recovery strategy templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-strategy-template-uib-ws.md)**

    The Recovery strategy template form is used to create reusable templates that can be applied to recovery strategies across loss scenarios and business continuity plans.

-   **[Task template integration in plan templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-a-bcp-template-uib-ws.md)**

    Plan templates support two synchronization options: Plan scope asset synchronization and Loss scenario asset synchronization with recovery strategy assets.

-   **[Related lists for Plan templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/plan-template-form.md)**

    The Plan templates record has the following related lists:

    -   Task template groups
    -   Task templates
-   **[Related lists for Loss scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-loss-scenario-recovery-task-bcp-uib-ws.md)**

    The Loss scenarios record has the following related lists:

    -   Task template groups
    -   Task templates
    -   Recovery strategies
    -   Plan templates
-   **[Related lists for Recovery strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-recovery-strategy-for-loss-scenario-uib-ws.md)**

    The Recovery strategies record has the following related lists:

    -   Task template groups
    -   Task templates
    -   Loss scenarios
    -   Plan templates
-   **[Recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-quick-recovery-task.md)**

    The recovery task list includes four additional columns: Plan loss scenario, Plan recovery strategy, Tag, and Task group. Use these columns to filter, group, and report on recovery tasks by scenario, strategy, or template group.

    The recovery task list toolbar includes **Insert** \(with Select task template groups\), **Save as group** \(with Add to group and Save tasks sub-options\), and **Add groups** for bulk insertion of task template groups.

    The Create a quick recovery task panel includes a Phase, Plan recovery strategy, All assets from plan, and a Planned duration field accepting hours, minutes, and seconds. The All assets from plan field can be narrowed to a subset of assets when a task applies to only part of the plan.

    A Gantt view is available on the **Recovery tasks** tab of a plan record.

-   **Event task list toolbar [Import export options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/export-import-event-tasks-using-excel.md)**

    The event task list toolbar adds **Export to Excel** and **Import from Excel** actions for managing tasks in bulk and switching between list and Gantt views.

-   **Loss scenario Recovery tasks tab [Loss scenario — Recovery tasks tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-loss-scenario-recovery-task-bcp-uib-ws.md)**

    Each loss scenario record includes a **Recovery tasks** tab that lists only the recovery tasks scoped to that scenario.


## Changed in the Australia release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


For more information, see [Business Continuity Management and ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-and-store.md).

## Activation information

Install Business Continuity Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

