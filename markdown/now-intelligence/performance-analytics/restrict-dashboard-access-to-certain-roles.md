---
title: Restrict responsive dashboard access to specific roles
description: Specify additional roles required to access the dashboard when you share a dashboard with specified users, groups, and roles. Only users who the dashboard has been shared with and who have one of the specified roles are able to access the dashboard.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dashboard permissions, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Restrict responsive dashboard access to specific roles

Specify additional roles required to access the dashboard when you share a dashboard with specified users, groups, and roles. Only users who the dashboard has been shared with and who have one of the specified roles are able to access the dashboard.

## Before you begin

Role required: pa\_admin, pa\_power\_user, admin, or be the dashboard owner. Other users who edit the dashboard can see this field but cannot modify it.

**Note:** Restricting access to a dashboard to specific roles is not the same as sharing the dashboard with those roles. You must share the dashboard before you can restrict access to specified roles. The best practice, however, is to use the **Share** panel to share with users, groups, and roles. Restrict to roles is not recommended.

The **Restrict to roles** field is available only after responsive dashboards have been enabled. If responsive dashboards have been enabled and then disabled, the **Restrict to roles** field remains available but does not affect dashboard access.

## About this task

When dashboards are migrated between releases, this field is automatically populated with the pa\_viewer and pa\_contributor roles to ensure that only users who could access the dashboard before migration can access it afterward.

## Procedure

1.  Navigate to the dashboard to restrict to specific roles.

2.  Click the context menu \(![Context menu icon](../../../common/image/Form_MenuIcon.png)\) and select **Dashboard properties**.

3.  In the **Restrict to roles** field, specify the additional roles required to access the dashboard.

    Users with any of the specified roles can access the dashboard only if it has been shared with them first from the **Share** panel. For more information, see [Share a responsive dashboard](t_ControlAccessToADashboard.md).


## Result

Only users with the restricted role are able to view the dashboard. A message on the Sharing panel indicates which roles have access. Click the roles in this message to view the properties of the dashboard.

![Restricted roles message in the Sharing panel](../image/dashboard-restricted-to-roles.png)

**Note:** The ability of users to share dashboards may be limited by the administrator. For more information, see [Responsive dashboard properties](../reference/dashboard-properties.md).

