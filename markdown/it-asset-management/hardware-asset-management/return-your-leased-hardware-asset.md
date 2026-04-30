---
title: Return your leased hardware asset
description: Return your hardware asset before the contract expires and avoid paying a penalty.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Manage your expiring contracts for leased hardware assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Return your leased hardware asset

Return your hardware asset before the contract expires and avoid paying a penalty.

## Before you begin

Role required: asset, itil, contract\_manager, inventory\_admin, or ham\_admin

## About this task

After you choose to return your leased asset, various Contract Asset tasks are created to take care of the return process for leased assets. Close each task to go to the next and to complete the process.

## Procedure

1.  Open a lease record.

<table id="choicetable_fkk_5d3_4xb"><thead><tr><th align="left" id="d193182e56">

UI

</th><th align="left" id="d193182e59">

Action

</th></tr></thead><tbody><tr><td id="d193182e65">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Contract** &gt; **Contracts** &gt; **Leases**.
2.  Select a lease record.


</td></tr><tr><td id="d193182e98">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Contract management**.
2.  Select the **Leases** related list and select a lease record.


</td></tr></tbody>
</table>2.  Select the Leased Assets related list.

3.  Select an asset.

4.  Under the **Contract Asset Tasks** tab, select the Planning task.

5.  On the Contract Asset Task form, select **Return** from the Lease action list.

6.  Change the **State** to **Closed Complete**.

    To take a lease action, you can follow any of the ways mentioned in [Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md).

    A Collection task is generated under the **Contract Asset Tasks** related list.

7.  Select the Collection task.

8.  If you successfully collected the asset, then do the following:

    1.  Select the **Asset collection** tab.

    2.  Set the **Asset collected** field to **Yes**.

    3.  In the **Stockroom** field, enter the stockroom where the asset is stored.

    On the Hardware form of the leased asset, the asset is moved to the In stock state and to the Pending transfer substate.

9.  If you haven’t collected the asset from your user, then do the following:

    1.  Update the **Asset collected** field to **No**.

        The **Action change** field appears under the **Asset collection** tab.

    2.  If you’re unable to collect the leased asset from your user and you want to buy out the leased asset, select **Buyout** from the Action change list.

        Further buyout-related tasks are created to take care of the buyout process. See [Buy out your leased hardware asset](purchase-your-leased-hw-asset.md).

    3.  If you’re unable to collect the leased asset from your user, and if you want to extend the lease contract, select **Extend** from the Action change list.

        Further extension-related tasks are created to take care of the lease extension process. See [Extend your lease contract](extend-your-lease-contract.md).

    4.  If you’re unable to collect the leased asset from your user and the leaser agrees that you return another similar asset, then do the following:

        1.  Select **Like-kind return** from the Action change list.

            On the original asset, the **Like-kind exchange** field is populated and the asset moves to the Missing state.

        2.  From the **Like-kind returned asset** field, select the asset that you want to return to the leaser.
        3.  From the **Stockroom** field, select the stockroom that contains the like asset that you want to return.
        Further return-related tasks are created for the like asset to take care of the return process.

        In the Hardware form, the following changes occur:

        -   The asset is moved to the Missing state.
        -   The like asset is moved to the In stock state and to the Pending transfer substate.
10. On the Collection task form, close the task.

    During the return confirmation, if there’s a need of settlement, you can update the **Settlement** field to **Yes** and update the **Settlement amount** field with the settlement cost. If you do this, a Return Settlement task and a Purchase order are then generated. After the Purchase order is moved to the Received state, the Settlement task is closed automatically.

    After the Collection task is closed, a Preparation task is created to remove device allocations of the asset.

11. Under the **Contract Asset Tasks** related list, open the Preparation task.

12. On the form, change the **State** field to **Closed Complete**.

    After the Preparation task is closed, a Shipment task is created to update the shipment details.

13. Under the **Contract Asset Tasks** related list, open the Shipment task.

14. Update the **Shipping carrier**, **Ship date**, and **Tracking number** fields.

15. Close the Shipment task.

    A Return Confirmation task is created. On the Hardware form, the leased asset is moved to the In transit state and to the None substate.

16. Under the **Contract Asset Tasks** related list, open the Return Confirmation task and do the following:

    1.  Set the **State** field to **Closed Complete**.

    2.  Set the **Return confirmation** field to **Yes**.


## Result

The Return Confirmation task is automatically assigned to the contract administrator. If necessary, you can assign it to any other user.

On the Hardware form of the leased asset, the asset is moved to the Retired state and to the Lease return substate.

**Parent Topic:**[Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md)

