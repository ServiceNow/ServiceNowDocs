---
title: Track an asset for a work order task from a mobile device
description: Track the status of an asset that you used to execute a work order task or an asset that you removed or replaced by using the Now Mobile Agent application on a mobile device. You can track the status of these assets as you're doing the task from a task location.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Inventory on Mobile Agent, Complete work orders on Mobile Agent, Using Field Service Management, Field Service Management]
---

# Track an asset for a work order task from a mobile device

Track the status of an asset that you used to execute a work order task or an asset that you removed or replaced by using the Now Mobile Agent application on a mobile device. You can track the status of these assets as you're doing the task from a task location.

## Before you begin

The work order task must be in the **Accepted** or **Work in Progress** state before you can do this procedure.

Role required: wm\_agent

## About this task

When you record the asset usage, the following actions occur:

-   The Use Part screen displays the assets in the Reserved Part and Available Part list in your inventory and shows the state as **In Stock** and the substate as **Reserved** and **Available**.
-   The Remove Part list displays the assets for all the companies and locations for the work order or work order tasks that you’re working on where the state of the part is **In Stock** and the substate is **Defective**.

## Procedure

1.  Open the Now Mobile Agent application.

2.  Tap **My Work**.

3.  In the My Tasks section, tap **See All**.

4.  Select the work order task that you want to track the assets for.

    The **Asset** field of the work order task inherits the asset details from its parent work order. If you add an asset to a work order, all its work order tasks are updated with the same asset details.

5.  View the parts used, the parts removed, and the part requirements for a work task by tapping **Parts**.

6.  Record information about the usage of an asset, the removal of an asset, or the replacement of an asset by tapping one of the following options.

    |Option|Details|
    |------|-------|
    |**Use Part**|Record the usage of an asset.|
    |**Remove Part**|Record the removal of an asset.|
    |**Swap Part**|Record the replacement of an asset.|

7.  Record the information about the usage or removal of an asset by tapping one of the following options.

<table id="choicetable_jdq_whz_4fb"><thead><tr><th align="left" id="d26936e197">

Option

</th><th align="left" id="d26936e200">

Details

</th></tr></thead><tbody><tr><td id="d26936e206">

**Record asset usage**

</td><td>

Record the usage of an asset:

-   Manually record the usage of an asset by selecting the part from your inventory, swiping to the left, and selecting **Use Part**.
-   Scan the asset tag to record the asset usage:
    1.  Select the part record.
    2.  Tap the more actions \(![More actions icon.](../image/OverflowIcon.png)\) icon and select **Scan Part** to scan a single part, or select **Scan Multiple Parts** to scan the barcodes of more than one part sequentially.

**Note:** You can scan a maximum of five parts sequentially. To change the limit for your requirements, see [Configure a grouped input for multiple scans](https://www.servicenow.com/docs/access?context=sg-configure-multiscan&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).

    3.  Select **Scan Asset Tag**.
    4.  Point the viewfinder rectangle on a bar code to scan the asset. The bar code digits are automatically recorded in the scanner.
    5.  Accept the scanned bar code by tapping the done icon.
    6.  Go back to the Use Part screen by tapping the back icon.
 The asset is added to the Asset Usages related list and the state for the part changes to **In Use**.

</td></tr><tr><td id="d26936e277">

**Record asset removal**

</td><td>

Record the removal of an asset:

-   Manually record the removal of an asset:
    1.  Select **Remove Part**.
    2.  Tap the add icon \(\) on the part record.
    3.  On the Remove part screen, select **Defective** in the **Removed part status** field.
    4.  If the part is consumable, enter the quantity that you want to replace.
    5.  In the **Drop off stockroom** field, select the stock room location.
    6.  Select **Remove Part**.
-   Scan the asset tag to record the removal of an asset:
    1.  Select **Remove part**.
    2.  Select **Scan to remove**.
    3.  Tap the overflow icon \(![Overflow Icon.](../image/OverflowIcon.png)\) and then to scan a part, select **Scan to remove**.

**Note:** You can scan a maximum of five parts sequentially. To change the limit for your requirements, see [Configure a grouped input for multiple scans](https://www.servicenow.com/docs/access?context=sg-configure-multiscan&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).

    4.  Tap the **Part to remove** field, and then select **Scan**.
    5.  Point the viewfinder rectangle on a bar code to scan the asset. The bar code digits are automatically recorded in the scanner.
    6.  Accept the scanned bar code by tapping the done icon.
    7.  Select **Review tab** and then to remove the part, tap the delete icon \(\).
    8.  Select **Submit**.
    9.  Go back to the Remove Part screen by tapping the back icon.
 The asset is removed from the Asset Usages related list and the state for the part changes to **In Stock** and the substate changes to **Defective**.

</td></tr><tr><td id="d26936e405">

**Record asset replacement**

</td><td>

Record the replacement of an asset:

-   Manually record the replacement of an asset:
    1.  Select **Swap part**.
    2.  Tap the add icon \(\) on the part record.
    3.  On the Swap part screen, select **Defective** in the **Removed part status** field if the part is faulty. Select **Available** if the part is non-defective.
    4.  Enter the quantity that you want to replace if the part is consumable.
    5.  In the **Drop off stockroom** field, select the stock room location.
    6.  Select the part that you want to replace by tapping the **Swap with** field.
    7.  In the Select part to swap screen, enter the asset tag number of the part in the **Search** field.
    8.  Tap the part record.
    9.  Select **Submit**.
-   Scan the asset tag to record the asset replacement:
    1.  Select **Swap part**.
    2.  Select **Scan to swap** to scan a part.
    3.  Tap the **Part to remove** field, and then select **Scan**.
    4.  Point the viewfinder rectangle on a bar code to scan the asset. The bar code digits are automatically recorded in the scanner.
    5.  Accept the scanned bar code by tapping the done icon.
    6.  Tap the **Swap with** field, and then select **Scan**.
    7.  Point the viewfinder rectangle on a bar code to scan the asset. The bar code digits are automatically recorded in the scanner.
    8.  Tap the done icon to accept the scanned bar code.
    9.  Select **Review tab** and verify the parts that you want to swap.
    10. Select **Submit**.
    11. Go back to the Remove Part screen by tapping the back icon.
 The new asset is added to the Asset Usages related list with the status of **In Use**.

 The asset is removed from the Asset Usages related list, the state for the part changes to **In Stock**, and the substate changes to **Defective**.

</td></tr></tbody>
</table>
**Parent Topic:**[Inventory on Mobile Agent](../concept/easily-track-parts.md)

**Related topics**  


[Record asset usage](../../planning-and-policy/task/t_RecordAssetUsage.md)

