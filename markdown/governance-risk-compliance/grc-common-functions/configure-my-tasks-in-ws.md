---
title: Monitor my tasks in the Tasks page in the workspace
description: Configure and monitor the tasks that are related to an assigned user in the workspace. Configure the landing pages and the widgets that are displayed in the workspaces using the Landing Page Configurations module. The configurations performed using the Landing Page Configurations module help you to filter the data that is displayed in different workspaces.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [My tasks in the workspace, Common GRC features, Governance, Risk, and Compliance]
---

# Monitor my tasks in the Tasks page in the workspace

Configure and monitor the tasks that are related to an assigned user in the workspace. Configure the landing pages and the widgets that are displayed in the workspaces using the Landing Page Configurations module. The configurations performed using the Landing Page Configurations module help you to filter the data that is displayed in different workspaces.

## Before you begin

Role required: sn\_grc.admin, sn\_grc\_workspace.task\_admin, sn\_grc\_workspace.task\_reader

## About this task

Navigate to the individual workspaces to view the tasks, items, and watchlist for the individual users and user groups.

## Procedure

1.  Navigate to the right workspace in one of the following ways:

    -   **All** &gt; **Audit** &gt; **Audit Workspace**.
    -   **All** &gt; **Operational Resilience** &gt; **Operational Resilience Workspace**.
    -   **All** &gt; **Policy and Compliance** &gt; **Compliance workspace**.
    -   **All** &gt; **Privacy** &gt; **Privacy workspace**.
    -   **All** &gt; **Regulatory Change Management** &gt; **Compliance workspace**.
    -   **All** &gt; **Risk** &gt; **Risk workspace**.
    -   **All** &gt; **Risk** &gt; **Risk Portal**.
    -   **All** &gt; **Vendor Management** &gt; **Workspace**.
2.  To navigate to the Tasks page, select the tasks icon \(![tasks icon in workspace.](../image/tasks-icon-new.png)\).

3.  Navigate to the tab that you want to view, and monitor the tasks.

    The Tasks page displays a timestamp showing when the task data was last refreshed, and a notification appears when the page is refreshing data in the background. The Tasks page displays the following tabs based on the workspace configuration:

    -   **My pending tasks**: Monitor the pending tasks assigned to you. The **Applicable Tables** tab under the **My pending tasks** tab on the Tasks Page Configuration module displays the list of tables that are applicable to the tasks. If the data is relevant to the user and if it matches the defined conditions, then it is populated under the **My pending task** tab in the workspace UI.

        If there is no data pertaining to you or if you do not have any assigned tasks, no data is not displayed under the **My pending tasks** tab. Only open and active tasks assigned to you're listed under the **My pending tasks** tab.

    -   **My group’s tasks**: Monitor the tasks assigned to the user groups that you belong to. The My group's task page displays the pending tasks assigned to the user groups that you belong to. When there are no pending tasks for the user group, a message displays that All tasks are completed. Select the group from the list for which you want to filter the tasks.
    -   **My items**: Monitor the tasks assigned to you and the issues reported by you. The My items tab displays the list of items that are either created by you or opened by you.
    -   **Watchlist**: Monitor the tasks for which you're in the watchlist. The My watchlist tab configuration displays the list of the tasks for which you're in the watchlist.
    -   **Confidential records**: Mark sensitive records as confidential and ensure that the right people have access to these records. The Confidential records tab configuration displays the confidential records for the selected table.
    **Note:** When a user or user group does not have any pending or associated tasks, a message displays under the respective tab that `All your tasks are done`.


**Parent Topic:**[My tasks in the workspace](../concept/configuration-of-tasks.md)

