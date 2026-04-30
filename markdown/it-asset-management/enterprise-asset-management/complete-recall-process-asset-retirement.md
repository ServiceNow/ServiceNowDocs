---
title: Complete the recall process for an enterprise asset through an asset retirement
description: Perform all tasks that are required for an asset retirement so that you can complete the recall process for an enterprise asset that has been recalled by the asset vendor.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Completing a recall order for your enterprise assets, Managing recalled enterprise assets, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the recall process for an enterprise asset through an asset retirement

Perform all tasks that are required for an asset retirement so that you can complete the recall process for an enterprise asset that has been recalled by the asset vendor.

## Before you begin

Before you can proceed with retiring a recalled enterprise asset, you must complete the Prepare task for that asset. See [Complete the Prepare task for a recalled enterprise asset](complete-prepare-task-recall-order.md) for detailed instructions.

Role required: sn\_eam.enterprise\_asset\_manager or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  Select the **Recall orders** tab.

3.  From the list of available recall orders, select the recall order that you want to complete.

    The recall order record opens.

4.  On the **Enterprise Recalled Assets** tab of the recall order record, select the enterprise asset that you want to retire.

    The enterprise recalled asset record opens.

5.  Complete and close the Retire task for the recalled enterprise asset.

    To successfully complete and close this task, you must retire and move the recalled enterprise asset to an available stockroom.

    1.  On the **Enterprise Recall Tasks** tab of the enterprise recalled asset record, select the task number for the **Retire** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the enterprise recalled asset record header.![Current task field.](../image/current-task-recall-orders.png)

        The Retire task opens.

    2.  On the **Details** tab of the Retire task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Recall task details|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Scheduled date|Date and time at which you plan to retire the enterprise asset.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Close the Retire task.

        You can either close the Retire task for only the specified enterprise asset or bulk update and close the Retire task for multiple enterprise assets.

        If you want to close the Retire task for only the specified enterprise asset, select **Close Task**.

        If you want to bulk update and close the Retire task for multiple enterprise assets, select **Include more assets**. When the Select assets for bulk update dialog box opens, select the check box for each enterprise asset that you want to bulk update and close the Retire task for. Select **Close Task** to close the dialog box and return to the Retire task.

        **Important:** You can bulk update the Retire task only for enterprise assets that have the same task name, state, assignment group, and assigned to user.

        The Retire task automatically reloads with an updated state of Closed Complete.


## Result

The enterprise recalled asset record moves to the Completed stage. In addition, the state and substate fields change to Retired and Pending disposal in the corresponding asset record.

## What to do next

Complete the asset retirement by disposing of the recalled enterprise asset using a disposal order. See [Create a disposal order in the Enterprise Asset Workspace](create-eamdisposal-order.md) for detailed instructions.

After you successfully dispose of the recalled enterprise asset, you can complete the recall process for all remaining enterprise assets that are included in the recall order. After all corresponding enterprise recalled asset records reach the Completed stage, the state of the recall order changes to Completed.

**Parent Topic:**[Completing a recall order for your enterprise assets](../concept/completing-recall-order-enterprise-assets.md)

