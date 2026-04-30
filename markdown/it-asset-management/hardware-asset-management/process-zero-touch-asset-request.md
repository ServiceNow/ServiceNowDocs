---
title: Process a Zero Touch Refresh request
description: Process a Zero Touch Refresh request to receive the assets from your provider and complete the Zero Touch Refresh flow.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage refresh of assets using Zero Touch Refresh, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Process a Zero Touch Refresh request

Process a Zero Touch Refresh request to receive the assets from your provider and complete the Zero Touch Refresh flow.

## Before you begin

The Service Exchange configuration necessary for the Zero Touch Refresh flow must have been set up. For more details, see [Service Exchange configuration for Zero Touch Refresh](../concept/service-bridge-config-ztr.md).

Role required: admin, asset, procurement\_user, or inventory\_user.

## About this task

After the provider ships the assets, the Zero Touch Refresh flow completes when the following actions have occurred:

1.  The employee confirms that the replacement asset is received.
2.  The inventory manager or the asset manager confirms and evaluates the old asset that was received.

## Procedure

1.  Log in to your ServiceNow® instance.

2.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

3.  From the **Zero touch refresh list**, select **Requests**.

4.  Select the request that you want to process.

5.  Select the **Zero Touch Refresh Tasks** tab.

6.  As a stockroom manager, notify the employee that the new asset is ready for pickup.

    1.  Select the **Ready for pickup** task.

    2.  Select **Close Task**.

    -   An email message is sent to notify the employee that the asset has arrived in the stockroom and is ready for pickup.
    -   The Receive asset task is created.
7.  Ensure that the Receive asset task is closed.

    -   If the employee has acknowledged receipt of the replacement asset online, the task is closed automatically.

        For more details, see [Acknowledge receipt of an asset on a mobile device](receive-assets-from-ztr.md) or [Acknowledge receipt of an asset through the Core UI](acknowledge-asset-core-ui.md).

    -   If the asset has been picked up at the stockroom but the employee has not acknowledged receipt online, users with the admin or asset role can close this task on behalf of the employee by accessing the task and selecting **Close task**.
8.  Confirm that the old asset was returned to the stockroom.

    1.  Select the Receive return asset task.

    2.  Select **Close task**.

    -   The Receive asset task is closed.
    -   The Asset evaluation task is created.
9.  Evaluate the old asset and select the appropriate status.

    1.  Select the Asset evaluation task.

    2.  In the **Evaluation status**, mark the asset for reuse, repair, or ready for disposal.

        -   To mark the asset for reuse, select **Re-deployable**.

            The state and substate of the asset are set to In stock and Available.

        -   To mark the asset for repair, select **Needs repair**.

            This option initiates the [Return Merchandise Authorization](../concept/return-merchandise-authorization.md) \(RMA\) flow.

            The state and substate of the asset are set to In stock and Pending repair.

        -   To mark the asset as ready for disposal, select **To be disposed**.

            The state and substate of the asset are set to In stock and Pending disposal.

    3.  Select **Close task**.


## Result

The Zero Touch Refresh flow completes. The stage and state of the Zero Touch Refresh request change to Closed complete and Completed.

**Parent Topic:**[Manage refresh of assets using Zero Touch Refresh](../concept/refresh-hardware-uisng-ztr.md)

**Related topics**  


[Configure replacement models for a refresh model](create-replacement-model.md)

[Request a hardware asset refresh through Zero Touch Refresh](create-zero-touch-refresh-request.md)

[Fulfill a Zero Touch Refresh Fulfillment Request](process-zero-touch-refresh-order.md)

[Acknowledge receipt of an asset on a mobile device](receive-assets-from-ztr.md)

[Acknowledge receipt of an asset through the Core UI](acknowledge-asset-core-ui.md)

