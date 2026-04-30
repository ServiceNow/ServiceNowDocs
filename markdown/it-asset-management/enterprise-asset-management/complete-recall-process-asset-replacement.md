---
title: Complete the recall process for an enterprise asset through an asset replacement
description: Work with your asset vendor to perform all tasks that are required for an asset replacement so that you can complete the recall process for an enterprise asset that has been recalled by the vendor.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Completing a recall order for your enterprise assets, Managing recalled enterprise assets, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the recall process for an enterprise asset through an asset replacement

Work with your asset vendor to perform all tasks that are required for an asset replacement so that you can complete the recall process for an enterprise asset that has been recalled by the vendor.

## Before you begin

Before you can proceed with replacing a recalled enterprise asset, you must complete the Prepare task for that asset. See [Complete the Prepare task for a recalled enterprise asset](complete-prepare-task-recall-order.md) for detailed instructions.

Role required: sn\_eam.enterprise\_asset\_manager or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Inventory view.

2.  Select the **Recall orders** tab.

3.  From the list of available recall orders, select the recall order that you want to complete.

    The recall order record opens.

4.  On the **Enterprise Recalled Assets** tab of the recall order record, select the enterprise asset that you want to replace.

    The enterprise recalled asset record opens.

5.  Complete and close the Receive New task for the recalled enterprise asset.

    To successfully complete and close this task, you must receive the new enterprise asset from the asset vendor. In addition, you must create an asset record for the new enterprise asset. See [Create enterprise assets](create-asset-eam.md) for detailed instructions.

    **Note:** When you create the asset record for the new enterprise asset, you must set the **State** field to **In stock**. You must also verify that the **Acquisition method** field is set to **Recall Replacement.**

    1.  On the **Enterprise Recall Tasks** tab of the enterprise recalled asset record, select the task number for the **Receive New** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the enterprise recalled asset record header.![Current task field.](../image/current-task-recall-orders.png)

        The Receive New task opens.

    2.  On the **Details** tab of the Receive New task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Recall task details|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Scheduled date|Date and time at which you plan to receive the new enterprise asset.|
        |Replacement asset|
        |Replacement asset|New enterprise asset that is replacing the recalled enterprise asset.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Select **Close Task**.

        The Receive New task automatically reloads with an updated state of Closed Complete.

    4.  Close the Receive New task to return to the enterprise recalled asset record.

6.  Complete and close the Replace task for the recalled enterprise asset.

    To successfully complete and close this task, you must replace the recalled enterprise asset with the new asset.

    1.  On the **Enterprise Recall Tasks** tab of the enterprise recalled asset record, select the task number for the **Replace** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the enterprise recalled asset record header.![Current task field.](../image/current-task-recall-orders.png)

        The Replace task opens.

    2.  On the **Details** tab of the Replace task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Recall task details|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Scheduled date|Date and time at which you plan to replace the recalled enterprise asset with the new asset.|
        |Replacement asset|
        |Replacement asset|New asset that has replaced the recalled enterprise asset.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Close the Replace task.

        You can either close the Replace task for only the specified enterprise asset or bulk update and close the Replace task for multiple enterprise assets.

        If you want to close the Replace task for only the specified enterprise asset, select **Close Task**.

        If you want to bulk update and close the Replace task for multiple enterprise assets, select **Include more assets**. When the Select assets for bulk update dialog box opens, select the check box for each enterprise asset that you want to bulk update and close the Replace task for. Select **Close Task** to close the dialog box and return to the Replace task.

        **Important:** You can bulk update the Replace task only for enterprise assets that have the same task name, state, assignment group, and assigned to user.

        The Replace task automatically reloads with an updated state of Closed Complete.

    4.  Close the Replace task to return to the enterprise recalled asset record.

7.  Complete and close the Ship Old task for the recalled enterprise asset.

    To successfully complete and close this task, you must ship the recalled enterprise asset back to the asset vendor.

    1.  On the **Enterprise Recall Tasks** tab of the enterprise recalled asset record, select the task number for the **Ship Old** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the enterprise recalled asset record header.![Current task field.](../image/current-task-recall-orders.png)

        The Ship Old task opens.

    2.  On the **Details** tab of the Ship Old task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Recall task details|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Scheduled date|Date and time at which you plan to ship the recalled enterprise asset back to the asset vendor.|
        |Shipment|
        |Carrier|Shipping carrier through which you shipped the recalled enterprise asset.|
        |Ship date|Date on which you shipped the recalled enterprise asset.|
        |Tracking number|Tracking number that enables you to track the status and location of the shipment.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Close the Ship Old task.

        You can either close the Ship Old task for only the specified enterprise asset or bulk update and close the Ship Old task for multiple enterprise assets.

        If you want to close the Ship Old task for only the specified enterprise asset, select **Close Task**.

        If you want to bulk update and close the Ship Old task for multiple enterprise assets, select **Include more assets**. When the Select assets for bulk update dialog box opens, select the check box for each enterprise asset that you want to bulk update and close the Ship Old task for. Select **Close Task** to close the dialog box and return to the Ship Old task.

        **Important:** You can bulk update the Ship Old task only for enterprise assets that have the same task name, state, assignment group, and assigned to user.

        The Ship Old task automatically reloads with an updated state of Closed Complete.


## Result

The enterprise recalled asset record moves to the Completed stage. The Enterprise Asset Management application then automatically retires the recalled enterprise asset, triggering the state and substate fields to change to Retired and Vendor credit in the corresponding asset record.

## What to do next

Complete the recall process for all remaining enterprise assets that are included in the recall order. After all corresponding enterprise recalled asset records reach the Completed stage, the state of the recall order changes to Completed.

**Parent Topic:**[Completing a recall order for your enterprise assets](../concept/completing-recall-order-enterprise-assets.md)

