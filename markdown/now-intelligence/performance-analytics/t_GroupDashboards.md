---
title: Organize dashboards into groups
description: Assign dashboards to groups so that users can find the dashboards they want more easily. Dashboard groups determine how dashboards appear in the dashboard picker when you navigate to Self-Service Dashboards . You can also add view permissions to dashboard groups.Dashboard group and dashboard permissions are not additive. Depending on how permissions are defined on a dashboard, dashboard group permissions may not apply.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Organize dashboards into groups

Assign dashboards to groups so that users can find the dashboards they want more easily. Dashboard groups determine how dashboards appear in the dashboard picker when you navigate to **Self-Service** &gt; **Dashboards**. You can also add view permissions to dashboard groups.

## Before you begin

Role required: admin, pa\_admin, or pa\_power\_user.

## About this task

Permissions on dashboard groups apply to all the dashboards in that group.

**Note:**

-   View permissions on an individual dashboard override the permissions set at the dashboard group level.
-   Edit permissions on a dashboard can affect or override the dashboard group permissions.
-   Dashboard group permissions do not appear in the dashboard Sharing panel.

To show single groups in the dashboard picker, add the parameter `sysparm_group=` followed by the group name to the dashboard URL. For example, to show only a dashboard group named incident, use the URL `https://<instance>/$dashboards.do?sysparm_group=incident`.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **System** &gt; **Dashboard Administration**.

    Review current dashboards groupings using the **Group** column. Dashboards without groups assigned to them show `(empty)` in the **Group** column. On the Dashboard Overview, these dashboards are grouped as Other.

2.  Select the name of the dashboard that you want to add to a group to open its form.

3.  In the **Group** field, use the lookup icon \(![Lookup icon](../image/icon-search.png)\) to select a group to add the dashboard to.

    Select an existing dashboard group or select **New** to create a dashboard group.

    ![Animated gif shows searching for a dashboard group and creating a new dashboard group](../image/add-db-group.gif)

4.  Open the form of the dashboard group to modify its permissions.

    Only view permissions can be set on dashboard groups.

    Dashboard groups use standard platform permissions. For more information, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).

5.  Select **Update**.


## How dashboard and dashboard group permissions interact on responsive dashboards

Dashboard group and dashboard permissions are not additive. Depending on how permissions are defined on a dashboard, dashboard group permissions may not apply.

If a dashboard belongs to a dashboard group, any view permissions defined on the dashboard override all view permissions on the dashboard group. Permissions on the dashboard group level are not visible from the **Share** panel of a dashboard. When you change the view permissions of a dashboard in a group, always review the dashboard group permissions to ensure that users do not lose access. For more information, see [Dashboard permissions scenarios](../../performance-analytics/task/troubleshoot-dashboard-permissions.md#).

For example, the dashboard group Support Dashboards contains the dashboards Open Incidents and Incident Metrics. The dashboard group has view permissions for the group Support. When you give view permissions to user John Dee for the dashboard Incident Metrics, the group Support can no longer see that dashboard. View permissions on the dashboard override all view permissions on the dashboard group.

