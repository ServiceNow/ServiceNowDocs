---
title: Complete the end of life workflow request for your software product
description: Perform all the tasks that are required to remove the end of life \(EOL\) software products from your asset inventory. If you set the Action field to Remove EOL Software in the Decide on IT strategy task, you must perform these software EOL tasks.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Complete the end of life workflow request for your software product

Perform all the tasks that are required to remove the end of life \(EOL\) software products from your asset inventory. If you set the **Action** field to **Remove EOL Software** in the Decide on IT strategy task, you must perform these software EOL tasks.

## Before you begin

Before you proceed with removing the EOL software, you must start an EOL workflow request. For details, see [Create an end of life workflow request for your software products](manage-eol-risk.md).

Role required: sam\_user, users with an itil role to whom a task is assigned

## About this task

To close an EOL request, you have to close and complete all the tasks required to complete the workflow. The following procedure explains how to close the EOL request, when you set the **Action** field to **Remove EOL Software** in the Decide on IT strategy task. You can apply the same approach to close the EOL request for the following possible values in the **Action** field in the Decide on IT strategy task:

-   Upgrade
-   Purchase support
-   Move to Azure
-   Accept risk

Additionally, the EOL workflow can be completed using the Software End of Life Flow in the Flow Designer application. You can customize the Software End of Life Flow according to your requirement by creating a copy of the flow and customizing the copy that you have created.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **Software Asset Analytics** &gt; **Lifecycle management**.

2.  On the Lifecycle management dashboard, open the End of life \(EOL\) products page by selecting the **Upcoming end of life product lifecycles in next 18 months** report or the **Current and past end of life product lifecycles** report.

3.  From the list of available EOL products, select the product for which you want to complete the EOL workflow.

4.  On the product record, select the **Software EOL Requests** tab.

5.  From the list of available software EOL requests, select the request number for which you want to complete the tasks.

6.  Complete the first task, which is the Assess IT architecture impact task.

    ![Software EOL tasks in the list view on the Software EOL Tasks tab.](../image/eol-tasks.png)

    1.  On the **Software EOL tasks** tab, select the task number for the Assess IT architecture impact task.

    2.  On the **Details** tab of the Assess IT architecture impact task, fill in the fields.

        For details on the form fields and their description, see [Software EOL tasks tab](../reference/software-eol-request.md#section_l11_yb1_4bc).

    3.  Complete the subtasks for the Assess IT architecture impact task by selecting the **Software EOL Subtasks** tab.

        **Note:** If a parent task includes subtasks, you must close all the subtasks. After you close all the subtasks, the parent task is automatically updated with a state of Closed Complete. Additionally, a new task appears on the **Software EOL tasks** tab only after you have closed and completed the preceding task.

7.  Complete the Assess IT security impact task.

    1.  On the **Software EOL tasks** tab, select the task number for the Assess IT security impact task.

    2.  On the **Details** tab of the Assess IT security impact task, fill in the fields.

        For details on the form fields and their description, see [Software EOL tasks tab](../reference/software-eol-request.md#section_l11_yb1_4bc).

    3.  Complete the subtasks for the Assess IT security impact task by selecting the **Software EOL Subtasks** tab.

8.  Complete the Decide on IT strategy task.

    1.  On the **Software EOL tasks** tab, select the task number for the Decide on IT strategy task.

    2.  On the **Details** tab, select **Remove EOL software** in the **Action** field.

        For details on the form fields and their description, see [Software EOL tasks tab](../reference/software-eol-request.md#section_l11_yb1_4bc).

    3.  Select **Close Task**.

        The Decide on IT strategy task is automatically updated with a state of Closed Complete. The corresponding Assess software licensing impact task appears in the list view on the **Software EOL Tasks** tab.

9.  Complete the Assess software licensing impact task.

    1.  On the **Software EOL tasks** tab, select the task number for the Assess software licensing impact task.

    2.  On the **Details** tab of the Assess software licensing impact task, fill in the fields.

        For details on the form fields and their description, see [Software EOL tasks tab](../reference/software-eol-request.md#section_l11_yb1_4bc).

    3.  Select **Close Task**.

        The Assess software licensing impact task is automatically updated with a state of Closed Complete. The corresponding Complete secure backup task appears in the list view on the **Software EOL Tasks** tab.

10. Complete the Complete secure backup task.

    1.  On the **Software EOL tasks** tab, select the task number for the Complete secure backup task.

    2.  On the **Details** tab of the Complete secure backup task, fill in the fields.

        For details on the form fields and their description, see [Software EOL tasks tab](../reference/software-eol-request.md#section_l11_yb1_4bc).

    3.  Select **Close Task**.

        The Complete secure backup task is automatically updated with a state of Closed Complete. The corresponding Create IT change plans task appears in the list view on the **Software EOL Tasks** tab.

11. Complete the Create IT change plans task.

    1.  On the **Software EOL tasks** tab, select the task number for the Create IT change plans task.

    2.  On the **Details** tab of the Create IT change plans task, fill in the fields.

        For details on the form fields and their description, see [Software EOL tasks tab](../reference/software-eol-request.md#section_l11_yb1_4bc).

    3.  Select **Close Task**.

        The Create IT change plans task is automatically updated with a state of Closed Complete. A change request appears on the **Change Requests** tab.

12. Select the change request and review the values that are automatically populated in the Change Request form.

    For details on completing a change request, see [Process a change request](https://www.servicenow.com/docs/access?context=t_ProcessAChangeRequest&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).


## Result

After the change request is complete, the workflow request is also complete.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

