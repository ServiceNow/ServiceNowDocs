---
title: Buy out your leased hardware asset
description: Buy out your leased hardware asset before the contract expires and avoid paying a penalty.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage your expiring contracts for leased hardware assets, Use, Hardware Asset Management, IT Asset Management]
---

# Buy out your leased hardware asset

Buy out your leased hardware asset before the contract expires and avoid paying a penalty.

## Before you begin

Role required: asset, itil, contract\_manager, inventory\_admin, or ham\_admin

## About this task

After you choose to buy out your leased asset, various Contract Asset tasks are created to take care of the purchase process for leased assets. Close each task to go to the next task and to complete the process.

**Note:** To close the Buyout tasks, the Purchase order that is created for the leased asset must be approved by the Procurement manager.

## Procedure

1.  Navigate to **All** &gt; **Contract** &gt; **Contracts** &gt; **Leases**.

2.  Click the Leased Assets related list.

3.  Open an asset.

4.  Under the **Contract Asset Tasks** related list, open the Planning task.

5.  On the Contract Asset Task form, select **Buyout** from the Lease action list.

6.  Change the **State** to **Closed Complete**.

    To take a lease action, you can follow any of the ways mentioned in [Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md).

    The Purchase order and Purchase order lines are created. In the Purchase order form, the **PO Type** field under the Details section is set to **Lease buyout**. You can order the Purchase orders only after completing all the asset tasks that are associated with the line items of the Purchase order.

    After receiving the Purchase orders, Expense lines are created to track the cost of the buyout.

    If the lease Buyout Purchase order of your contract is in the Requested state, and if some assets covered under the same contract are updated with the Buyout lease action, then the Purchase order lines of the assets covered are appended to the Purchase order. A new purchase order is created only if an existing Purchase order for a lease buyout is not in the Requested state.

    A Buyout task is created to update the buyout information.

7.  Under the **Contract Asset Tasks** related list, open the Buyout task.

8.  Under the **Buyout details** tab, do the following:

    1.  Update the **Buyout date** field with the date on which you want to purchase the asset.

    2.  Update the **Buyout amount** field with the amount to purchase the asset.

9.  Fill in the fields as required.

10. Change the **State** field to **Closed Complete**.

    After you update the **Cost** field on the Purchase order line, the **Buyout amount** field is automatically populated with the same amount. You can change the **Cost** field on the Purchase order line until the Buyout task is closed.

    A Buyout Confirmation task is created to take care of the confirmation process.

11. Under the **Contract Asset Tasks** related list, open the Buyout Confirmation task and do the following:

    1.  Fill in the required fields.

    2.  Update the **Buyout confirmation field** to **Yes**.

    3.  Change the **State** field to **Closed and Complete**.

    If you want to change the **Buyout amount** field from the Buyout Confirmation task form, you can change the amount from the Purchase order.

    To close the Buyout Confirmation task, the Purchase order must be in the Received state.


## Result

After a buyout is confirmed, the following changes occur in the asset record under the **Financial** tab:

-   The **Cost** field is updated to the buyout amount.
-   The **Acquisition method** field is changed to Purchase.

**Parent Topic:**[Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md)

