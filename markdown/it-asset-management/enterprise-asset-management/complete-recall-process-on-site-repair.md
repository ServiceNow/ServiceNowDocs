---
title: Complete the recall process for an enterprise asset through an on-site repair
description: Perform all tasks that are required for an on-site repair so that you can complete the recall process for an enterprise asset that has been recalled by the asset vendor.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Completing a recall order for your enterprise assets, Managing recalled enterprise assets, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the recall process for an enterprise asset through an on-site repair

Perform all tasks that are required for an on-site repair so that you can complete the recall process for an enterprise asset that has been recalled by the asset vendor.

## Before you begin

Before you can proceed with repairing a recalled enterprise asset on-site, you must complete the Prepare task for that asset. See [Complete the Prepare task for a recalled enterprise asset](complete-prepare-task-recall-order.md) for detailed instructions.

Role required: sn\_eam.enterprise\_asset\_manager or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  Select the **Recall orders** tab.

3.  From the list of available recall orders, select the recall order that you want to complete.

    The recall order record opens.

4.  On the **Recalled Assets** tab of the recall order record, select the enterprise asset that you want to repair.

    The recalled asset record opens.

5.  Complete and close the On-site Repair task for the recalled enterprise asset.

    To successfully complete and close this task, you must repair the recalled enterprise asset on-site.

    1.  On the **Recall Tasks** tab of the recalled asset record, select the task number for the **On-site Repair** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the recalled asset record header.![Current task field.](../image/current-task-recall-orders.png)

        The On-site Repair task opens.

    2.  On the **Details** tab of the On-site Repair task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Recall task details|
        |Remediation action|Option that indicates how you want to proceed with the recall process for the enterprise asset. This field is automatically set to **On-site Repair**.|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Scheduled date|Date and time at which you plan to perform the on-site repair.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Close the On-site Repair task.

        You can either close the On-site Repair task for only the specified enterprise asset or bulk update and close the On-site Repair task for multiple enterprise assets.

        If you want to close the On-site Repair task for only the specified enterprise asset, select **Close Task**.

        If you want to bulk update and close the On-site Repair task for multiple enterprise assets, select **Include more assets**. When the Select assets for bulk update dialog box opens, select the check box for each enterprise asset that you want to bulk update and close the On-site Repair task for. Select **Close Task** to close the dialog box and return to the On-site Repair task.

        **Important:** You can bulk update the On-site Repair task only for enterprise assets that have the same task name, state, assignment group, and assigned to user.

        The On-site Repair task automatically reloads with an updated state of Closed Complete.


## Result

The recalled asset record moves to the Completed stage. In addition, the state and substate fields change to In stock and Available in the corresponding asset record.

## What to do next

Complete the recall process for all remaining enterprise assets that are included in the recall order. After all corresponding recalled asset records reach the Completed stage, the state of the recall order changes to Completed.

**Parent Topic:**[Completing a recall order for your enterprise assets](../concept/completing-recall-order-enterprise-assets.md)

