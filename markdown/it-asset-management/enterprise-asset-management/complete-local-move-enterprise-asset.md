---
title: Complete the local move for an enterprise asset
description: Perform all tasks that are required to move an enterprise asset without shipping it. You must perform these tasks if you set the Move type field to Local Move in an enterprise move line.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Completing an enterprise asset move order, Managing enterprise asset move orders, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Complete the local move for an enterprise asset

Perform all tasks that are required to move an enterprise asset without shipping it. You must perform these tasks if you set the **Move type** field to **Local Move** in an enterprise move line.

## Before you begin

Before you can proceed with the local move, you must complete the Prepare task for the enterprise asset. See [Complete the Prepare task for a moving enterprise asset](complete-prepare-task-moving-enterprise-asset.md) for detailed instructions.

Role required: sn\_eam.enterprise\_asset\_manager, sn\_eam.enterprise\_admin, or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, navigate to **Asset operations** &gt; **Moves** &gt; **Move orders**.

2.  From the list of available move orders, select the move order that you want to complete.

    The move order record opens.

3.  On the move order record, select the **Enterprise move lines** tab.

4.  From the list of available enterprise move lines, select the enterprise move line for the enterprise asset that you want to move.

    The enterprise move line record opens.

5.  Complete and close the Local move task for the enterprise move line.

    By default, this Local move task applies only to the enterprise asset that is associated with the given enterprise move line. If you want to apply the same Local move task to additional enterprise assets within your move order, you can include those assets in the task.

    To successfully complete and close this task, the enterprise asset must be moved to the target location without being shipped.

    1.  On the **Enterprise move tasks** tab, select the task number for the **Local move** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the enterprise move line record header.![Current task field.](../image/current-task-move-orders.png)

        The Local move task opens.

    2.  On the **Details** tab of the Local move task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Enterprise move task|
        |Assignment group|Group that the task is assigned to. This field populates automatically based on the group that the entire move order is assigned to.|
        |Assigned to|User who the task is assigned to. This field populates automatically based on the user who the entire move order is assigned to.|
        |Scheduled date|Date and time at which the task is scheduled to be completed.|
        |Priority|Priority of the task.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Close the task.

        -   To close the task without including additional enterprise assets from your move order, select **Close Task**.
        -   To close the task after including additional enterprise assets from your move order, use the following steps:
            1.  Select **Include more assets**.

                The Select assets dialog box opens.

            2.  In the dialog box, select the check box for each additional enterprise asset that you want to include.
            3.  Select **Close Task**.
    The Local move task is automatically updated with a state of Closed Complete.


## Result

The enterprise move line is automatically updated with a status of Completed.

## What to do next

Move all remaining enterprise assets that are included in the move order. After all corresponding enterprise move lines reach a status of Completed, the move order is complete.

**Parent Topic:**[Completing an enterprise asset move order](../concept/completing-enterprise-asset-move-order.md)

