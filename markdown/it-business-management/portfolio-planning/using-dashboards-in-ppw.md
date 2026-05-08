---
title: Using dashboards in Portfolio Planning
description: Using the Platform Analytics dashboards in Portfolio Planning Workspace, you can monitor performance, track progress, and make informed decisions related to planning and execution.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Portfolio Planning, Strategic Portfolio Management]
---

# Using dashboards in Portfolio Planning

Using the Platform Analytics dashboards in Portfolio Planning Workspace, you can monitor performance, track progress, and make informed decisions related to planning and execution.

## Roles required for managing dashboards

<table id="id_cld_xj5_xbc"><thead><tr><th>

Access level

</th><th>

Required roles

</th></tr></thead><tbody><tr><td>

Read, duplicate, or share the Execution Dashboard

</td><td>

sn\_align\_core.ap\_read\_only**Note:** To view data in financial-related and capacity-planning-related widgets, users must have the appropriate roles.

</td></tr><tr><td>

Edit the Execution Dashboard

</td><td>

admin

</td></tr></tbody>
</table><table id="table_lc2_x3h_cfc"><thead><tr><th>

Access level

</th><th>

Required roles

</th></tr></thead><tbody><tr><td>

Create dashboards

</td><td>

sn\_align\_core.apw\_user

</td></tr><tr><td>

Edit dashboards

</td><td>

sn\_align\_core.apw\_user**Note:** You can edit dashboards that you own or those you’ve been granted permission to edit.

</td></tr></tbody>
</table>**Note:** You can create widgets in dashboards by configuring any available data source table in the ServiceNow AI Platform. However, you must have read access to the source tables to view key data, metrics, or visualizations.

For example, if you create a widget in a dashboard configuring the Cost Plan Breakdown table to display budget data, the budget summary is visible on the dashboard only if you have read access to the Cost Plan Breakdown table. Similarly, when you share this dashboard with a stakeholder, the stakeholder must also have read access to the Cost Plan Breakdown table to view the budget summary.

For more information on the required roles to manage Platform Analytics dashboards, see Platform Analytics dashboard roles.

-   **[Execution Dashboard in Portfolio Planning Workspace](../../portfolio-planning/concept/execution-dashboard-ppw.md)**  
The Execution Dashboard helps portfolio and product managers gain real-time visibility into delivery progress across work items, enabling portfolio leads to detect delays, course-correct early, and keep the strategy on track.
-   **[View a dashboard in Portfolio Planning Workspace](../task/view-dashboard-ppw.md)**  
View key data and metrics on a dashboard to monitor performance, track progress, and make informed decisions related to planning and execution.
-   **[Create a dashboard](../task/create-dashboard-ppw.md)**  
In the Platform Analytics experience, you can create shareable dashboards with data visualizations, filters, and other elements. You can use the available elements in the inline editor to create different types of widgets as needed.
-   **[Duplicate a dashboard](../task/copy-dashboard-ppw.md)**  
If the dashboard you want to create is similar to an existing one, duplicating the existing dashboard saves your time. After duplicating the dashboard, you can customize the tabs and widgets as required.
-   **[Share a dashboard](../task/share-dashboard-ppw.md)**  
Share a dashboard with stakeholders, planning managers, portfolio managers, or product managers to provide visibility into work progress and foster collaboration. You can grant either view-only rights or both view and edit rights to a shared dashboard.
-   **[Add a Platform Analytics dashboard](../task/add-platform-dashboard-to-ppw.md)**  
If you have existing dashboards created using Platform Analytics, you can add them to the Portfolio Planning Workspace to access them directly from a single location.

**Parent Topic:**[Portfolio Planning](../../portfolio-planning/concept/portfolio-planning-app-landing-page.md)

