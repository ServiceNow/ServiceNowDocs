---
title: Solving permissions issues on a responsive dashboard
description: Dashboard permissions can be set in several different locations.Permissions on dashboards can be complicated. If you set a permission on a dashboard group, for example, permissions set on a dashboard within that group override it. This matrix shows what is visible based on various combinations of permissions.Users with edit permissions on a responsive dashboard may also need edit permissions on another dashboard that the tab is used in.Dashboards in scoped applications may not be visible to non-admin users. Non-admin users may not be able to view the dashboard or the widgets on the dashboard don't load.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Dashboard permissions, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Solving permissions issues on a responsive dashboard

Dashboard permissions can be set in several different locations.

## Before you begin

When you find problems with permissions on responsive dashboards, you can review permissions on the Dashboard Sharing panel, group permissions, and dashboard properties.

Role required: dashboard\_admin, pa\_admin

## Procedure

-   Check the permissions on the Dashboard Sharing pane.

    The dashboard owner, users with the dashboard\_admin or admin role, and users with the pa\_power\_user or pa\_admin role who can edit the dashboard can perform this step.

-   Review the permissions of the group to which the dashboard belongs.

    Dashboard group permissions do not show up in the dashboard Sharing panel.

    Users with the dashboard\_admin, admin, pa\_power\_user, or pa\_admin role can perform this step.

-   Compare the dashboard and dashboard group permissions.

    If permissions are specified on a dashboard, the permissions on the dashboard group are overridden and no do not apply.

    Users with the dashboard\_admin, admin, pa\_power\_user, or pa\_admin role can perform this step.

-   On the dashboard properties form, review the roles specified in the **Restrict to roles** field.

    Only users with one of the roles specified in this field can view the dashboard.

    The dashboard owner, users with the dashboard\_admin or admin role, and users with pa\_power\_user or pa\_admin roles who can edit the dashboard can perform this step. Other users who can edit the dashboard can view this field but cannot edit it.


## Dashboard permissions scenarios

Permissions on dashboards can be complicated. If you set a permission on a dashboard group, for example, permissions set on a dashboard within that group override it. This matrix shows what is visible based on various combinations of permissions.

The Dashboard permissions scenarios table uses these abbreviations:

-   DB = Dashboard
-   DG = Dashboard Group
-   RTR = Restrict to Roles

    For more information, see [Restrict responsive dashboard access to specific roles](../../dashboards/task/restrict-dashboard-access-to-certain-roles.md).

-   X = Unspecified

**Note:** Users with admin and dashboard\_admin roles have full permissions on all dashboards.

|Scenario|DG|DG Permission|DB view permission|DB edit permission|RTR|Who can view the DB?|
|--------|---|-------------|------------------|------------------|---|--------------------|
|No DG, no DB permissions|X|X|X|X|X|Only the owner|
|Only RTR|X|X|X|X|asset|Only the owner|
|Only DB permissions|X|X|itil|X|X|Users with the itil role|
|DB permissions and RTR|X|X|itil|X|asset|Users with both the itil AND asset roles|
|Only DG without permissions|Exists|X|X|X|X|Users with either the pa\_admin role OR the pa\_power\_user role|
|DG without permissions and RTR|Exists|X|X|X|asset|Users with both the asset role AND either the pa\_admin role OR the pa\_power\_user role|
|Only DG and DG permissions|Exists|itil|X|X|X|Users with either the itil role OR the pa\_admin role OR the pa\_power\_user role|
|DG, DG permissions, and RTR|Exists|itil|X|X|asset|Users with both the asset role AND either the itil role OR the pa\_admin role OR the pa\_power\_user role|
|DG, DG permissions, and DB permissions|Exists|itil|itil\_admin|X|asset|Users with both the itil\_admin role AND the asset role|
|DG, DG permissions, DB permissions, and RTR|Exists|itil|itil\_admin|X|X|Users with the itil\_admin role|

The default permissions for a dashboard group are pa\_admin and pa\_power\_user. If a permission, such as itil, is specified on the dashboard group, this permission is added to the default permission. Permissions on individual dashboards override the dashboard group permission.

## Solving issue with edit permissions on responsive dashboards

Users with edit permissions on a responsive dashboard may also need edit permissions on another dashboard that the tab is used in.

### Before you begin

Role required: admin

### About this task

A dashboard is shared with a user with edit permissions. On some tabs, the user cannot add widgets. When the user selects **Add widgets**, nothing happens. The same user is able to add widgets to other tabs and dashboards. The cause for the problem is related to how the affected dashboard tab was created. If the dashboard tab was created in a [non-responsive dashboard](../../dashboards/concept/non-responsive-dashboards.md) and the tab is linked to another dashboard tab, the affected user needs editing permissions on this other linked dashboard.

### Procedure

1.  Navigate to the affected dashboard.

2.  From the context menu ![](../../dashboards/image/icon-context-p.png), select **Dashboard Properties**.

3.  Select Launch Dependency Assessment.

    The results show the dashboard and all the tabs used by the dashboard.

4.  Select the affected tab.

5.  From the context menu ![](../../dashboards/image/icon-context-p.png), choose **Show Used By**.

    The result shows the dashboards where the tab appears.

6.  Open the other dashboard that uses the affected tab.

7.  Edit sharing permissions on that dashboard and to give edit access to the affected user.


### Result

The affected user can now edit the dashboard tab on the responsive dashboard.

## Solving issues with shared dashboards in non-global scopes

Dashboards in scoped applications may not be visible to non-admin users. Non-admin users may not be able to view the dashboard or the widgets on the dashboard don't load.

### Before you begin

Role required: admin of the associated scoped application.

### About this task

Users may see the message 'Dashboard hasn't been shared with user' or 'This dashboard is restricted to the following roles,' without a list of roles.

### Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Set the system property glide.security.scoped\_administration.honor\_global\_acl to true.

    If this property is already set to true, no update is necessary.

3.  As application administrator, switch the scope to the scope the dashboard was created in.

4.  Navigate **All** &gt; **sys\_scoped\_admin\_acl\_inheritance.list**.

5.  If reports have the same issue, create records for these tables:

    -   Reports \[sys\_report\]
    -   Report Users and Groups \[sys\_report\_users\_groups\]
6.  Create records for these tables:

    -   Dashboard \[pa\_dashboards\]
    -   Portal Page \[sys\_portal\_page\]
    -   Tabs \[pa\_tabs\]
    -   Dashboard Permissions \[pa\_dashboards\_permissions\]

