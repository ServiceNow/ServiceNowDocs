---
title: Tasks Page Configuration module
description: The Tasks Page Configuration module in the classic user interface displays the configurations related to the Tasks section in the landing pages of the workspaces. The configurations in the Tasks Page Configuration module help the users to view the data in different workspaces.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Landing Page Configurations module, Common GRC features, Governance, Risk, and Compliance]
---

# Tasks Page Configuration module

The Tasks Page Configuration module in the classic user interface displays the configurations related to the Tasks section in the landing pages of the workspaces. The configurations in the Tasks Page Configuration module help the users to view the data in different workspaces.

Only users with the sn\_grc\_workspace.task\_admin role can configure the Tasks landing pages for the workspaces using the Tasks Page Configurations module in the classic user interface. The administrators are assigned the sn\_grc\_workspace.task\_admin role by default.

GRC administrators perform task page configurations, including the workspaces, tabs, and filters configurations in this module. Based on all the filter conditions that are applied at table levels or state levels, the users can view the data in the Tasks landing page in the workspace.

In the homepage view of the workspace, the widgets displayed about the tasks such as My tasks and My group's work are configured using the UI Builder. Clicking these widgets in the homepage view directs the users to the Tasks page in the workspace.

For the Audit workspace, Compliance workspace, Privacy workspace, and Risk workspace, the following pre-configured tabs are shipped by default:

-   My pending tasks
-   My group's tasks
-   My items
-   Watchlist

Starting with GRC: Common Workspace Elements application version 14.x, the administrators with the sn\_grc\_workspace.task\_admin role can add or remove the tabs in the Task Configuration record. They can also prioritize or order the tabs in a sequence. When a tab is created in the Task Configuration record under the Tasks Page Configuration module, it is displayed in the workspace UI.

The task administrators can change the order of the tabs in the UI. If the same order is configured for two tabs, the tabs are displayed in an alphabetical order.

The following image shows the updated Task Configuration record.

![Task Configuration](../image/task-page-config-module-new-button.png "Task Configuration record")

GRC administrators can configure the names of the task configuration records that are displayed in the landing pages. Administrators can do the following:

-   Update the name and description of the record in the classic user interface. Only administrators can view this data in the classic user interface. End users cannot view this data in the workspace view.
-   Update the title of the workspace that is displayed in the Tasks landing page in the workspace. End users can view this data in the workspace view.
-   Update the title of the applicable table, filter condition, and column names.
-   Update the filter conditions for the tabs.
-   Filter the records based on the group selection for the applicable table.
-   Add, update, remove, or override the state labels of the tables.
-   Update the type of the tab such as group tab or regular tab.

**Parent Topic:**[Landing Page Configurations module](../../grc-common/reference/admin-config-using-grc-common.md)

