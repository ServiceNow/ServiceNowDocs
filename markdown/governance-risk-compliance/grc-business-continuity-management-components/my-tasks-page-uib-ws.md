---
title: My tasks page view
description: My tasks page displays a single-pane view of your pending tasks, tasks assigned to your user group, and the tasks that are on your watchlist.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [BCM Configurable Workspace, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# My tasks page view

My tasks page displays a single-pane view of your pending tasks, tasks assigned to your user group, and the tasks that are on your watchlist.

## Tabs in the Tasks page

The Tasks page displays the assigned tasks for the logged-in user in different tabs as shown in the example.

![My tasks page in BCM UIB Workspace.](../image/my-tasks-page-all-tabs.png)

The Tasks page in BCM UIB Workspace displays these tabs:

-   **My pending tasks**: Displays an overview of the pending tasks that are assigned to you and the tasks that require an action from you. You can filter pending tasks with the states:

    -   All
    -   Draft/New
    -   In progress
    -   Needs my approval
    -   Needs my review
    -   Overdue
    -   Pending response
    **Note:** The data displayed in the Tasks page is based on the roles of the users.

-   **My items**: Displays a list of the tasks that are assigned to the logged-in user.

-   **Watchlist**: Displays a list of the tasks for which you are on the watchlist. When a task is approved or completed, you receive a notification on the **Watchlist** tab.


A typical My tasks page for a logged-in user is shown in the example.

![My tasks page.](../image/my-tasks-bcm-ws.png)

For more information on the My tasks page configurations module in the application, see [My tasks page configurations](my-tasks-page-config-module.md).

**Note:** On the **My pending tasks**, **My items**, and **Watchlist** tabs, you can only view the records that are in-progress. The closed and canceled records are not displayed on these tabs. You can view the closed and canceled records in their respective forms in BCM UIB Workspace.

If you have the BCM administrator role, you can customize BCM UIB Workspace by updating the Tasks page configurations module. To update the Tasks page configurations, you can navigate to **All &gt; General administration &gt; My tasks page configuration** in your instance.

If you have the BCM manager or BCM user roles, you can also get relevant recommendations on your business continuity tasks on the Home page.

To view more information on the Tasks Page Configuration, see [Update the Tasks Page Configuration record](../../grc-common/task/view-tasks-page-configurations.md).

