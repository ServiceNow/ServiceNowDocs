---
title: My tasks in the workspace
description: GRC administrators can configure the tasks for the individual users and user groups in the GRC Landing Page Configurations module. Based on these configurations, the workspace users can view the individual user tasks, user group tasks, my items, and watchlist on the Tasks page in the workspace view.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# My tasks in the workspace

GRC administrators can configure the tasks for the individual users and user groups in the GRC Landing Page Configurations module. Based on these configurations, the workspace users can view the individual user tasks, user group tasks, my items, and watchlist on the Tasks page in the workspace view.

The roles required to configure and view the workspaces are listed below.

|Role|Actions associated with the role for the workspace|
|----|--------------------------------------------------|
|sn\_grc.admin, sn\_grc\_workspace.task\_admin|Configure the Tasks Page Configuration records in all the workspaces.|
|sn\_grc.business\_user|View the Tasks page in the Risk Portal workspace.|
|sn\_audit\_ws.supervisor, sn\_audit\_ws.auditor,|View the Tasks page in the Audit workspace.|
|sn\_compliance.admin|Configure and view the Tasks page in the Compliance workspace.|
|sn\_oper\_res.admin|Configure and view the Tasks page in the Operational Resilience workspace.|
|sn\_privacy.admin|Configure and view the Tasks page in the Privacy workspace.|
|sn\_grc\_reg\_change.it\_admin|View the Tasks page in the Compliance workspace.|
|sn\_risk\_workspace.IT\_risk\_manager and sn\_risk\_workspace.operational\_risk\_manager,|View the Tasks page in the Risk workspace.|
|sn\_vdr\_risk\_asmt.vendor\_risk\_manager|View the Tasks page in the Vendor Management workspace.|

Based on the tasks that were set up by the administrators, the tasks are displayed under the following tabs in the configuration records for workspaces:

-   My pending tasks
-   My group's tasks
-   My items
-   Watchlist
-   Confidential records

**Note:** Task configurations are maintained in the Applicable Table, which now includes an Active/Inactive flag. The Active/Inactive flag determines whether a configuration is considered in My Tasks. When marked active, the configuration appears in the relevant task tabs such as My Pending Tasks or My Group Tasks; when marked inactive, it is excluded. This functionality enables you to control visibility without deleting records. Toggle the flag to activate or deactivate entries as needed.

You can view the Tasks page in the following workspaces:

-   Audit Workspace
-   Operational Resilience workspace
-   Policy and Compliance Workspace: Displayed under the Policy and Compliance module.
-   Privacy Workspace
-   Regulatory Change Management Workspace in Policy and Compliance Workspace
-   Risk Workspace
-   Risk Portal
-   Vendor Management Workspace

    **Note:** My items and Watchlist are not displayed in the Vendor Management Workspace.


-   **[Monitor my tasks in the Tasks page in the workspace](../task/configure-my-tasks-in-ws.md)**  
Configure and monitor the tasks that are related to an assigned user in the workspace. Configure the landing pages and the widgets that are displayed in the workspaces using the Landing Page Configurations module. The configurations performed using the Landing Page Configurations module help you to filter the data that is displayed in different workspaces.

**Parent Topic:**[Common Governance, Risk, and Compliance features](../../grc-common/concept/common-grc-features.md)

