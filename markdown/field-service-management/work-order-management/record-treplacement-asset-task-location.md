---
title: Track the replacement of an asset from a task location
description: Track the status of an asset that you replaced with another asset in a work order. You can track the status as you're doing the task from a task location.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View asset usage, Execute work order tasks, Updating task status in web interface, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Track the replacement of an asset from a task location

Track the status of an asset that you replaced with another asset in a work order. You can track the status as you're doing the task from a task location.

## Before you begin

Role required: wm\_agent

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Assigned to me**.

2.  Open a work order task.

3.  In the Asset Usages related list, display the Asset Usage form by selecting **Remove Asset**.

    The **Service order task** field displays the task number of the work order, and that the status of the asset is set to **Removed**.

4.  In the **Model** field, select a model.

    The **Quantity** and **Asset** fields are enabled or inactive depending on what you selected in the **Model** field.

5.  In the **Quantity** and **Asset** fields, enter the information about your consumable and non-consumable assets:

    -   If the model is consumable, enter the quantity that was removed in the **Quantity** field.
    -   If the model is non-consumable, select the asset that is listed in the **Asset** field.
6.  In the **Drop off stockroom** field, select the drop-off location where you want to drop off the asset.

7.  In the **Removed part status** field, select the status of the part that you want to remove.

    If the part is faulty, select **Defective**. If it's not faulty, select **Available**.

8.  In the **Replacement asset** field, select the asset that you want to replace.

9.  In the **Replacement model** field, select the model to replace the asset that you removed.

10. Select **Submit**.


## Result

Two asset records are added to the Asset Usages related list. The removed asset is added to the Asset Usages related list with a status of **Removed**. The replaced asset is also added to the Asset Usages related list.

**Parent Topic:**[View asset usage](t_RecordAssetUsage.md)

