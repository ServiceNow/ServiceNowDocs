---
title: Visualize recovery tasks on Gantt chart
description: Use the Gantt chart component on recovery task pages to provide a visual timeline view of tasks associated with the current plan. Customize the view by adding, removing, or reordering columns as needed. The chart is implemented as a UI page to enable customizations and to support multiple versions without requiring changes to existing page behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/view-gantt-chart-for-reco-tasks.html
release: australia
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 4
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Visualize recovery tasks on Gantt chart

Use the Gantt chart component on recovery task pages to provide a visual timeline view of tasks associated with the current plan. Customize the view by adding, removing, or reordering columns as needed. The chart is implemented as a UI page to enable customizations and to support multiple versions without requiring changes to existing page behavior.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Key behaviors:

-   The Gantt chart and the related list are displayed together to maintain feature parity.
-   Data displayed in the chart is scoped to the plan currently being viewed.
-   Column customization in the Gantt chart works the same way as in the list view.

The Gantt chart bars are drawn from the plan's **Planned start** date and each task's planned duration. Set the **Planned start** field on the plan's **Details** tab before opening the Gantt view; the field is labelled "Used to calculate the planned start time of tasks". The first task in the dependency chain begins at this date and time; each subsequent task begins when its dependencies finish.

\[Omitted image "planned-start-date.jpg"\] Alt text: Plan record Details tab with the Planned start field highlighted under General Information, showing the helper text "Used to calculate the planned start time of tasks".

## Procedure

1.  On the plan record, open the **Details** tab and set the **Planned start** date and time.

    The **Planned start** field is the anchor date used to calculate every task's planned start time on the Gantt chart. If it is empty, the chart still renders but task bars are not anchored to a real date.

2.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Plan record** &gt; **Recovery tasks**.

3.  Open the plan whose recovery tasks you want to visualize and open the Recovery tasks section.

    The Gantt chart is displayed alongside the related list. Both views are visible by default. The **Recovery tasks** tab toolbar provides access to the **Gantt** toggle, **Insert**, **Add groups**, and **Save as group** controls.

    \[Omitted image "qi-insert.png"\] Alt text: Recovery tasks tab on a plan record showing the toolbar with Gantt, Insert, Add groups, and List controls.

    \[Omitted image "gantt-list-view.jpg"\] Alt text: Recovery tasks tab showing the toolbar List, Insert, and Gantt controls, with Task 0, Task 1, Task 2.1, Task 2, and Task 2.2 in the planned order column.

4.  Select the settings icon and open the **Timeline** tab in the **Personalize** panel to choose a layout.

    The **Layout** drop-down offers three options:

    -   **Grid** — List view only \(the default when first opening the tab\).
    -   **Timeline** — Timeline bars only.
    -   **Grid and timeline** — List and timeline shown side by side. This is typically the easiest layout to read because the task order is visible next to the bars.
    \[Omitted image "timeline-layout-settings.jpg"\] Alt text: Personalize panel with the Timeline tab selected and the Layout drop-down expanded, showing Grid and timeline, Grid, and Timeline.

5.  Hover over a bar to see the task's planned start and end date in a tooltip.

    Each bar spans from the task's calculated start to its calculated end. Bars are colored by phase. The first task in the dependency chain starts at the plan's **Planned start**; each downstream task starts when its dependencies finish.

    \[Omitted image "gantt-timeline-with-grid.jpg"\] Alt text: Gantt chart in Grid and timeline layout, with a tooltip on a Task 0 bar showing Start date 2026-05-04 09:00:00 and End date 2026-05-05 09:00:00.

6.  To customize, select the column customization option \(same control used in the list view\) from the Gantt chart view.

7.  Add, remove, or reorder columns as needed.

8.  Select Apply or Save to confirm your column configuration.

9.  To act on an existing task without leaving the Gantt view, select the row-action menu \(the vertical ellipsis\) on the task row.

    The row-action menu is available only on the Gantt view; the standard list view does not expose custom row actions. The menu offers the following actions:

    -   **Edit** — Opens the quick-edit form for the selected task. Update fields such as **Phase** and select **Save**.
    -   **Insert before** — Opens the Create a quick recovery task modal with the **Insert task** drop-down set to **before** and the reference field pre-populated with the selected task.
    -   **Insert after** — Same as Insert before, with the drop-down set to **after**.
    -   **Insert in parallel** — Same as the others, with the drop-down set to **in parallel**.
    \[Omitted image "gantt-row-actions-edit.jpg"\] Alt text: Gantt chart row-action menu open on a recovery task row, showing Quick edit form.

    \[Omitted image "gantt-row-insert-before.jpg"\] Alt text: Create a quick recovery task modal launched from the Insert before row action; the Insert task drop-down is set to "before" and the reference field is pre-populated with Task 2.1.

10. To reorder using quick actions: select the task row’s action menu and choose Add after, Add before, or Add in parallel.

    The chart updates to reflect the new task order.


**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

