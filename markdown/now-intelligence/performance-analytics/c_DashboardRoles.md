---
title: Dashboard permissions
description: Dashboards have special granular view and edit permissions that are managed from the Sharing pane. Access control lists \(ACLs\) apply to most widgets that are added to dashboards.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Dashboard permissions

Dashboards have special granular view and edit permissions that are managed from the Sharing pane. Access control lists \(ACLs\) apply to most widgets that are added to dashboards.

-   Users with any role can create dashboards, share dashboards that they own with users and groups, and edit dashboards if they have been given edit permissions. Users with any role can restrict access by role to any dashboard that they have created. The user also needs whatever roles are necessary to access the specific data on the dashboards.
-   Users without a role can view dashboards that have been shared with them, but cannot create or edit dashboards.
-   Users with pa\_admin and pa\_power\_user roles can manage users, groups, and roles on any dashboard that they can edit. For more information, see [Performance Analytics roles](../../performance-analytics/reference/r_PARoles.md).
-   Users with the dashboard\_admin or admin role can edit and manage users, groups, and roles for any dashboard. Admin and dashboard\_admin users can also change a dashboard owner at any time.
-   Only a dashboard owner and users with the dashboard\_admin or admin role can delete that dashboard.
-   The ability of users to share dashboards may be limited by the administrator. For more information, see [Responsive dashboard properties](../reference/dashboard-properties.md).
-   If Explicit Roles are activated, dashboards are treated as internal resources. Users with the snc\_external role cannot view dashboards by default. For more information, see [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   Domain separation can affect the ability of users to edit dashboards that have been shared with them. For more information, see [Domain separation and responsive dashboards](domain-separation-in-dashboards.md).

| |View|Create|Edit|Share|Delete|
|---|----|------|----|-----|------|
|No role|Only dashboards that have been shared with them.|No|No|No|No|
|Any role|Dashboards that they create and that have been shared with them.|Yes|Only dashboards they have created or that have been shared with them with edit rights. Cannot add or remove Performance Analytics widgets without at least pa\_power\_user rights.|Only dashboards they have created and only with users and groups. The ability of users to share dashboards may be limited by the administrator. For more information, see [Responsive dashboard properties](../reference/dashboard-properties.md).|Only dashboards they own or have created.|
|admin|All|Yes|Edit and manage dashboard owners, users, groups, and roles for any dashboard.|Yes|Any dashboard|
|dashboard\_admin|All|Yes|Edit and manage dashboard owners, users, groups, and roles for any dashboard.|Yes|Any dashboard|
|pa\_admin|Dashboards that they create and that have been shared with them.|Yes|Only dashboards they have created or that have been shared with them with edit rights. Can add or remove Performance Analytics widgets.|Only dashboards they have created and only with users and groups. The ability of users to share dashboards may be limited by the administrator. For more information, see [Responsive dashboard properties](../reference/dashboard-properties.md).|Only dashboards they own or have created.|
|pa\_power\_user|Dashboards that they create and that have been shared with them.|Yes|Only dashboards they have created or that have been shared with them with edit rights. Can add or remove Performance Analytics widgets.|Only dashboards they have created and only with users and groups. The ability of users to share dashboards may be limited by the administrator. For more information, see [Responsive dashboard properties](../reference/dashboard-properties.md).|Only dashboards they own or have created.|
|Dashboard owner|Yes|N/A|Yes|Yes. The ability of users to share dashboards may be limited by the administrator. For more information, see [Responsive dashboard properties](../reference/dashboard-properties.md).|Only dashboards they have created.|

Widget ACLs apply when that widget is added to dashboards \(except for Performance Analytics widgets\). If a user can view a dashboard but does not have ACLs to view one of its widgets, an empty widget placeholder is displayed. ACLs do not apply to data visualizations that aggregate data, such as pie or bar reports. ACLs always apply to list data that is displayed in widgets. Rows in a list that a user does not have access to are not displayed.

**Note:** ACLs are not applied to Performance Analytics widgets that are added to dashboards. Any user who can view a dashboard can view all its Performance Analytics widgets. Performance Analytics widgets can only be added to dashboards by users with the pa\_power\_user, pa\_admin, and admin roles.

However, if a Performance Analytics widget displays real-time scores, the score each logged-in user sees depends on their roles and the ACLs of the facts table. For more information, see [Real-time scores](../../performance-analytics/concept/real-time-scores.md).

The **Restrict to role** field on the dashboard properties form and dashboard group permissions may have an impact on dashboard permissions. The dashboard owner, and users with pa\_power \_user, pa\_admin, or admin roles can change dashboard properties. Users with the pa\_power\_user, pa\_admin, and admin roles can change dashboard group permissions.

For example, when you add a pie report widget with 36 records to a dashboard, users who can access to that dashboard and that report can view the report of all 36 records. However, if a user drills down into the list view for that widget, only the records the user is allowed to access are visible.

**Related topics**  


[Restrict responsive dashboard access to specific roles](../task/restrict-dashboard-access-to-certain-roles.md)

[Organize dashboards into groups](../task/t_GroupDashboards.md#)

[Performance Analytics roles](../../performance-analytics/reference/r_PARoles.md)

[Administering reports](../../reporting/concept/c_AdminsteringReports.md)

