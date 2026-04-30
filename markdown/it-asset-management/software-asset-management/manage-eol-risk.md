---
title: Create an end of life workflow request for your software products
description: Manage risks associated with your software product installations that have reached the end of life \(EOL\) or are reaching EOL in the next 18 months. You can create an EOL request and take the required action for the EOL software.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Lifecycle management dashboard, Software asset analytics view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create an end of life workflow request for your software products

Manage risks associated with your software product installations that have reached the end of life \(EOL\) or are reaching EOL in the next 18 months. You can create an EOL request and take the required action for the EOL software.

## Before you begin

Role required:

-   Create or modify an EOL request: sam\_admin
-   Read an EOL request: sam\_user, users with an itil role to whom a task is assigned
-   Complete an EOL task: sam\_user, users with an itil role to whom a task is assigned

## About this task

When software products reach EOL, end of support, or end of extended support, their risk of failure increases. You can choose to remove such software products that are reaching or have reached EOL, upgrade them to the latest software version, or purchase additional support for their maintenance. The EOL workflow takes you through the process of completing your change request based on the action you choose for your EOL software products. If you want to purchase additional support for your EOL software, you can create a purchase order.

**Note:** You must have the Procurement plugin \(com.snc.procurement\) activated to complete a purchase order.

The EOL workflow can also be completed using the Software End of Life Flow in the Flow Designer application. You can customize the Software End of Life Flow according to your requirement by creating a copy of the flow and customizing the copy that you have created.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Lifecycle management**.

2.  On the [Lifecycle management dashboard](../concept/lifecycle-management-dashboard.md), select the **Upcoming end of life product lifecycles in next 18 months** report or the **Current and past end of life product lifecycles** report.

    The End of life products page displays the current and upcoming life-cycle phases calculated using the Software Product Lifecycle \[sam\_sw\_product\_lifecyle\] table. For more details, see [Software models and Software entitlements](../concept/software-models-and-entitlements.md).

3.  Select a record that has the **Current phase** as either End of Support, End of Extended Support, or End of Life.

    The Software Product Lifecycle report opens for the selected record.

    **Note:** You can also access the Software Product Lifecycle report by navigating to **Software Asset Workspace** &gt; **License usage** &gt; **Reports**.

4.  Create an EOL request by selecting **Manage EOL risk**.

    The product details in the Software EOL request form are populated from the Software Product Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table.

5.  On the Software EOL request form, fill in the fields.

    For details on the fields and descriptions, see [Software EOL request fields](../reference/software-eol-request.md).

6.  Start the EOL workflow to take required action for your EOL software.

    1.  Select **Start EOL Workflow**.

    2.  Select the **Software EOL Tasks** tab.

    3.  On the Software EOL task form, fill in the fields.

        For details on the form fields and descriptions, see [Software EOL tasks tab](../reference/software-eol-request.md#section_l11_yb1_4bc).

    4.  Complete the subtasks for the parent task by selecting the **Software EOL Subtasks** tab.

        **Note:** If a parent task has subtasks, you must close all the subtasks.

    5.  Repeat steps b through d for all the tasks listed on the **Software EOL Tasks** tab.

    -   If you select one of the following values in the **Action** field on the **Software EOL Tasks** tab, a change request is generated:

        -   Remove EOL software
        -   Upgrade
        -   Move to Azure
        For details on removing an EOL software product, see [Complete the end of life workflow request for your software product](complete-eol-workflow-request.md). For details on completing a change request and the role required for it, see [Process a change request](https://www.servicenow.com/docs/access?context=t_ProcessAChangeRequest&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

    -   If you select **Purchase support** in the **Action** field and select the **Auto create PO** option in the EOL task, a purchase order is created. For details on completing a purchase order and the role required for it, see [Create a purchase order line item](../../procurement/task/t_CreateAPurchaseOrderLineItem.md).
    After you complete the parent task, the **Stage** field is updated to reflect the stage of the task. Additionally, the **Action initiated** field is updated to reflect the action you have selected for the EOL request.

    **Note:** You can cancel the EOL workflow anytime by selecting the **More Actions** ellipsis icon and then selecting **Cancel EOL request**.


## Result

After the change request or the purchase order is complete, the workflow request is complete.

