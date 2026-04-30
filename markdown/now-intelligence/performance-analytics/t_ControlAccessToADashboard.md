---
title: Share a responsive dashboard
description: Share a dashboard with other users to create a shared view of data that you can use to collaborate. You can give other users viewing rights or both viewing and editing rights.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [allow a user access to a dashboard, determine dashboard access, share a dashboard]
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Share a responsive dashboard

Share a dashboard with other users to create a shared view of data that you can use to collaborate. You can give other users viewing rights or both viewing and editing rights.

## Before you begin

Role required:

-   You can share dashboards that you own with other groups and users.
-   Only users with the admin, dashboard\_admin, pa\_admin, or pa\_power\_user role can see roles in the **Sharing** panel.
-   Users with the pa\_admin or pa\_power\_user role can share dashboards that they can edit.
-   Users with the admin role can share any dashboard they can access.

**Note:** This topic refers to Dashboards in the Core UI. If your instance is migrated to Platform Analytics experience, see [Share a Platform Analytics dashboard](share-db-in-ac.md).

Access control list \(ACL\) rules for scoped applications apply to dashboards created within scoped applications. To apply pa\_dashboard ACLs to dashboards within a scoped app, see [Enable pa\_dashboard records in scoped applications](enable-pa-db-records-scoped-apps.md).

Reports and other data visualizations on dashboards are subject to report\_view ACLs and may not be visible to all users you share a dashboard with. For more information, see [Report\_view access control](../../reporting/concept/report-view-access-control.md).

Administrators can set two properties that affect how you share responsive dashboards:

-   **glide.cms.share\_dashboards.role**

    In this system property, the admin can specify a comma-separated list of roles that can share their own dashboards.

    **Note:** If one role in this list is misspelled, that role will not be able to share dashboards. If there is only one role in this list and that role is misspelled, no user will be able to share dashboards until the value for this property is corrected.

-   **glide.cms.dashboards.sharing\_with\_secure\_search**

    In this system property, the admin can specify that security rules are applied to the lists of users, user groups, and roles that are visible when users share responsive dashboards. Only users with one of these roles can see roles in the **Sharing** panel: admin, dashboard\_admin, pa\_admin, and pa\_power\_user.


For more information, see [Dashboard permissions](../concept/c_DashboardRoles.md).

## About this task

In general, when you share a dashboard, you aren’t granting permission to the widgets on that dashboard. Most Performance Analytics widgets, however, inherit security rules from the dashboards where they’ve been added. If you can view a dashboard, you can see the Performance Analytics widgets on that dashboard.

**Note:** Performance Analytics List widgets don’t show the indicators that you don’t have permission to read. While the dashboard permission applies to the whole Performance Analytics list widget, individual indicators in the widget follow the permissions for those indicators. For more information about indicator permissions, see [Control access to an indicator](../../performance-analytics/task/t_ControlAccessToAnIndicator.md).

When domain separation is enabled and the system property **glide.security.admin.override.accessterm** is not selected, admins must be in the same domain as the dashboard to share it. See [Evaluate the admin override at the access level](https://www.servicenow.com/docs/access?context=t_EvalAdmOverrideAccLevel&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Use the **Search dashboard** box to find the dashboard that you want to share.

3.  Select the Sharing icon \(![Sharing icon](../image/icon-share-db.png)\) to open the **Share** panel.

4.  Select **Add groups and users** \(![Add content icon](../image/icon-add-user-db.png)\). Users who have the admin, pa\_admin, dashboard\_admin, or pa\_power\_user roles can also see roles on the **Share** panel.

5.  Start typing the name in the **To** field.

6.  Select a user, group, or role from the displayed list.

7.  From the **Recipients** list, select **Can view** or **Can edit** to specify the permissions the user, group, or role has on the dashboard.

    When a person you’ve shared the dashboard with goes to the Dashboard Overview, they see either Viewer or Editor as their role on the dashboard.

    ![Sharing window with two recipients selected, the knowledge admin role selected, and the Recipients Can view menu item selected.](../image/invite-user-role-goup-to-dashboard1-p.png)

    **Note:** To edit a shared dashboard, a user must be in the same domain as the dashboard. Sharing a dashboard with write access \(**Can edit**\) doesn’t change that. The **Can edit** option only works if the dashboard is shared with a user in the same domain as the dashboard. For more information, see [Domain separation and responsive dashboards](../concept/domain-separation-in-dashboards.md).

8.  Clear the **Send an email invitation** check box.

    You can choose not to send an email message. For example, when recipients already know the dashboard has been shared with them.

    **Note:** Sending email from within your instance requires configuration of email servers. For more information, see [Basic email setup](https://www.servicenow.com/docs/access?context=c_StandardEmailConfiguration&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

9.  Write an addition to the default email invitation message.

    The default email message reads "The dashboard &lt;Name of Dashboard&gt; has been shared with you by &lt;user role&gt;."

    Users with the admin role can edit the default email message. Navigate to **System Notification** &gt; **Email** &gt; **Notifications** and open the dashboard sharing notification. For more information, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

10. Select **Share**.

    ![Share window with specified recipients, Send an email notification box checked, and an invitation message added.](../image/invite-user-role-goup-to-dashboard3-p.png)


## Result

The dashboard is shared and, if specified, an invitation is sent to the invited users.

