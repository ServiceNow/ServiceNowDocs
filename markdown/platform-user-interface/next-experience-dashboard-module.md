---
title: Create a Dashboard Module
description: Create custom dashboards for the All menu using the Next Experience All Menu Editor.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Next Experience All Menu Editing, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create a Dashboard Module

Create custom dashboards for the All menu using the Next Experience All Menu Editor.

## About this task

Build custom dashboards with the Dashboard module to visualize your data at a glance. Combine charts, images, lists, and other components into a unified view that delivers the insights you need instantly.

Common examples of dashboards you can build with the dashboard module:

-   Operational dashboards for managers
-   Analytics overview for a team
-   Role-specific dashboard

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**.

2.  Select the **Edit application** icon.

    ![Arrow pointing the edit application icon in the all menu.](../image/neame-edit-app.png)

3.  Select **+** in the menu header.

    ![Arrow pointing the add module icon in the header.](../image/neame-add-module.png)

4.  Add a dashboard module by hovering over the module and selecting **Add**.

5.  Select the dashboard module in the **Modules** pane.

6.  In the form, fill in the fields.

    |Field|User input|
    |-----|----------|
    |Name|Enter a name for the dashboard.|
    |Roles|Select which roles can access the application menu. If no roles are set, all users can see the menu when it's active.|
    |Hint|Enter a tooltip that describes the module when hovered over.|
    |Override app menu roles|Module roles override application roles when selected, displaying the module even if application menu roles wouldn't normally enable it.|

7.  Select **Done**.

8.  Select **Add new element**.

9.  Select the element that you want to add to your custom dashboard.

    In this example, add a **Data visualization** element.

10. Select **New Visualization**.

11. Select a **Visualization type**.

    In this example, select the **Horizontal bar**.

12. Select **+ Add data source**.

    For this example, select the **Task** table.

13. Select **+ Add custom conditions** to define conditions for the data source.

14. Select **Add this source**.

15. Select **Save**.

16. Select **Open module** in the top bar to preview the dashboard.

    ![Arrow pointing the open module icon in the header.](../image/neame-open-dashboard-module.png)


## What to do next

Continue building your dashboard by adding more elements such as additional visualizations, filters, or text components. Arrange and resize elements to create a balanced layout that provides users with a comprehensive view of their data.

**Parent Topic:**[Next Experience All Menu Editing](../concept/next-experience-all-menu-editing.md)

