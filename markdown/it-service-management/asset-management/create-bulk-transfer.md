---
title: Perform bulk updates for transfer order lines
description: Update tasks for multiple transfer order lines at one go to streamline the transfer order process.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Asset Management, IT Service Management]
---

# Perform bulk updates for transfer order lines

Update tasks for multiple transfer order lines at one go to streamline the transfer order process.

## Before you begin

Transfer order lines enable the transfer of multiple assets on a transfer order. When you create a transfer order line, a transfer order line task is automatically created. Transfer order line tasks are created to move transfer order lines from one stage to the other. Each transfer order line can have multiple tasks such as **Requested**, **Shipment Preparation**, **In Transit**. For information on the stages of a transfer order line task, see [Summary of transfer order line tasks](../concept/transfer-orders-asset.md#).

Role required: inventory\_user

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Order**.

2.  Select **Bulk Update** next to the Transfer Order Lines related list.

    The system property **sn\_itam\_tol\_bulk\_update\_max\_count** determines the maximum count of transfer order lines that would be processed during a single bulk update operation.

    The Bulk Update - Transfer Order Line dialog box appears.

3.  In the **Select a stage** field, select the stage that you want to move this task to.

    For example, if all the transfer order lines are currently in the **Draft** stage and you want to move them to the next stage, which is **Requested**, select **Requested** in the **Select a stage** field.

    All transfer order lines, along with the asset display names that are eligible to move to the selected stage appear in the **Available** box.

4.  In the **Assigned to** field, select the person you want to assign this task to.

    The **Assigned to** field defaults to the logged-in user.

5.  Select the transfer order lines in the **Available** box and move them to the **Selected** box.

    When you select the transfer order lines, you can view the model and asset display names for hardware and consumable assets. For consumable assets, you can view additional details such as quantity requested and quantity received.

6.  Select **Update**.

    All the selected transfer order line tasks and associated subtasks for the selected stage are closed and the next task in the process is created. For example, all the transfer order line tasks in the **Requested** stage are closed and the next task in the process **Shipment Preparation**, is created.

7.  Return to the Bulk Update - Transfer Order Line dialog box to continue this process until you close all the tasks required for completing the transfer order line.


**Parent Topic:**[Asset Management](../concept/c_AssetManagement.md)

