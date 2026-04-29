---
title: Manage responsive dashboards
description: Depending upon their role, users can delete or duplicate responsive dashboards, and remove a user from a dashboard. All users can mark a dashboard as a favorite.Delete dashboards that are no longer used. Deleted dashboards cannot be restored.When dashboard tabs are no longer useful, it is possible to delete them.When you duplicate a responsive dashboard, its widget layout is preserved. However, sharing permissions aren’t preserved. Changes you make to the duplicated dashboard don’t affect the original dashboard.Provide a more useful name for your dashboard by renaming it.When you no longer want to share a dashboard with specific users, groups, or roles, you can remove their access to the dashboard.You can mark a dashboard as a favorite to access it easily from the navigation pane.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [dashboard, delete a dashboard, how to clone a dashboard, duplicate a dashboard, copy a dashboard, set a dashboard favorite, bookmark a dashboard, favorite a dashboard]
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Manage responsive dashboards

Depending upon their role, users can delete or duplicate responsive dashboards, and remove a user from a dashboard. All users can mark a dashboard as a favorite.

## Delete a responsive dashboard

Delete dashboards that are no longer used. Deleted dashboards cannot be restored.

### Before you begin

Role required: dashboard\_admin or admin, or be the owner of the dashboard.

Inform any users that you have shared the dashboard with that you are deleting it. Users may have bookmarked the dashboard or marked it as a favorite. Those users see an error when they try to access a deleted dashboard.

**Note:** This topic refers to Dashboards in the Core UI. If your instance is migrated to Platform Analytics experience, see [Delete a Platform Analytics dashboard](delete-db-in-ac.md).

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the boxes next to the names of dashboards that you want to delete.

3.  Select **Delete** and confirm the deletion.


### Result

When you delete a dashboard, dashboard tabs that are not used on other dashboards are deleted.

### Delete a dashboard tab

When dashboard tabs are no longer useful, it is possible to delete them.

#### Before you begin

Role required: dashboard\_admin or admin. If you are the owner of the dashboard or otherwise have edit rights on the dashboard, you can also delete a dashboard tab.

#### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the dashboard containing the tab that you want to delete.

3.  To delete a dashboard tab, point to the tab and click the trash icon.


#### Result

When you delete a dashboard tab, it is removed from the dashboard. If it is not used in any other dashboard, it is deleted entirely.

## Copy a responsive dashboard

When you duplicate a responsive dashboard, its widget layout is preserved. However, sharing permissions aren’t preserved. Changes you make to the duplicated dashboard don’t affect the original dashboard.

### Before you begin

**Note:** This topic refers to Dashboards in the Core UI. If your instance is migrated to Platform Analytics experience, see [Duplicate a Platform Analytics dashboard](../../reporting/task/duplicate-db.md#).

Role required: Any user who can share a dashboard can copy it.

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the dashboard that you want to duplicate.

3.  From the context menu ![context menu icon](../../performance-analytics/image/ContextMenu.png) select **Duplicate Dashboard**.

    A copy of the dashboard is created with you as the owner. The name of the copy is Copy of \[Original Dashboard Name\].

4.  To rename the dashboard, select the context menu![context menu icon](../../performance-analytics/image/ContextMenu.png), select **Dashboard Properties**, and edit the **Name** field.


### Result

A copy of the dashboard is created with you as the owner.

### What to do next

Modify the dashboard and then share it with other users.

## Rename a responsive dashboard

Provide a more useful name for your dashboard by renaming it.

### Before you begin

Role required: Users can edit dashboards that they own, or ones that they have the right to edit. See [Dashboard permissions](../concept/c_DashboardRoles.md) for more information about viewing and editing rights on dashboards.

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  From the dashboard picker, select the dashboard that you want to rename.

3.  From the context menu \(![Context menu icon](../image/icon-context-p.png)\), select **Dashboard Properties**.

4.  In the name field, enter the new name for the dashboard.

5.  Select **Update**.

    **Note:** The **Owner** field is required. If this field is empty, provide the name of the dashboard's owner to complete this task.


## Remove a user from a dashboard

When you no longer want to share a dashboard with specific users, groups, or roles, you can remove their access to the dashboard.

### Before you begin

Role required: Any dashboard owner can remove users or groups from dashboards they own.

Users with the dashboard\_admin or admin role can remove users, groups, or roles from any dashboard.

Users with the pa\_admin or pa\_power\_user role can remove users, groups, or roles from any dashboard that they can edit. These dashboards include dashboards that a user owns, and dashboards to which they have been granted edit rights.

For more information, see [Dashboard permissions](../concept/c_DashboardRoles.md).

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the dashboard that you want to modify.

3.  Select the sharing icon \(![](../image/icon-share-db.png)\).

4.  In the **Share** panel, select the X next to the name of the user, group, or role that you want to remove.

    ![Sharing panel with X to remove a user from a dashboard highlighted with a 4 for step 4.](../image/remove-user-db-p.png)


### Result

The removed users no longer have the right to view the shared dashboard.

**Related topics**  


[Restrict responsive dashboard access to specific roles](restrict-dashboard-access-to-certain-roles.md)

## Mark a responsive dashboard as a favorite

You can mark a dashboard as a favorite to access it easily from the navigation pane.

### Before you begin

Anyone who can access a dashboard can make it a favorite.

Role required: none

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  From the dashboard picker, select the dashboard that you want to mark as a favorite.

3.  Select the context menu \(![](../image/icon-context-p.png)\) and select **Create Favorite**.


### Result

Favorite dashboards appear in the favorites tab of the application navigator.

