---
title: Tracking order tasks and associated projects
description: With the SPM integration, project managers and fulfillment agents or managers can track projects in Strategic Portfolio Management that have associated order tasks in Order Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/using-spm-integration.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Tracking order tasks and associated projects

With the SPM integration, project managers and fulfillment agents or managers can track projects in Strategic Portfolio Management that have associated order tasks in Order Management.

## Tracking projects for planned order tasks in SPM

As a project manager, you can review and update projects that have been created for tracking planned order tasks using the Project Portfolio Management application in SPM. When fulfillment managers and agents update or complete order tasks, Order Management automatically synchronizes project states between SPM and order line items, task and domain order states, and project task and order task states as fulfillment managers and agents complete order tasks.

A project manager has the it\_project\_manager role for tracking and updating projects.

<table id="table_yts_x1k_fyb"><thead><tr><th>

Task

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Review an order fulfillment project and state

</td><td>

1.  Navigate to **All** &gt; **Projects** &gt; **Project Workspace**.
2.  Select the project for the order item.

**Note:** The **Project Name** is the name assigned when Order Management created the project using the specified project template.

3.  Select the **Details** tab then scroll down to the **Project Tasks** tab to review project tasks, State, and Percent complete,

\[Omitted image "ppm-project-list-view-states.png"\] Alt text: List view that shows project tasks, state, and percent complete


</td></tr><tr><td>

Review the project state and project task state to assess the project status

</td><td>

1.  Navigate to **All** &gt; **Projects** &gt; **Project Workspace**.
2.  Select the project for the order item.
3.  Select the **Planning** tab.

The Gantt chart view displays.\[Omitted image "ppm-planning-console-gantt.png"\] Alt text: Gantt chart view of project task state for planned order tasks and status colors indicating if the task is within the planned end date


</td></tr><tr><td>

Review notes and comments on order tasks from fulfillment agents and managers

</td><td>

1.  Navigate to **All** &gt; **Projects** &gt; **Project Workspace**.
2.  Select the project for the order item.
3.  Go to the **Notes** tab and view the comments and status updates from Order Management.

</td></tr></tbody>
</table>## Tracking fulfillment tasks that have associated projects in Order Management

As a fulfillment agent or manager, you can view the relationship between a project and order line item, project tasks, and order task in the Configurable Workspace. You can also post notes and additional comments on order lines and order tasks to communicate with the project manager responsible for project oversight of the order management tasks.

|Task|Example|
|----|-------|
|View order line-to-project relationship in order line item form|\[Omitted image "order-line-relationship.png"\] Alt text: Order Line form view that shows Order Line Task Relationship|
|View project task-to-domain order relationship in domain form|\[Omitted image "domain-order-proj-relationship.png"\] Alt text: Domain order form that shows Project Task Oversight tab with parent child task details|
|View order task-to-project task relationship in order task from|\[Omitted image "order-task-proj-relationship.png"\] Alt text: Order task form that shows Project Task Oversight tab with parent child task details|
|View **Details** tab in order task relationship to see task number, project number, and order line item number relationship|\[Omitted image "ol-relationship-details-tab.png"\] Alt text: Order line task view that shows Details tab of order line task relationship|

