---
title: Extend your lease contract
description: Extend your lease contract before the contract expires and avoid paying a penalty.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage your expiring contracts for leased hardware assets, Use, Hardware Asset Management, IT Asset Management]
---

# Extend your lease contract

Extend your lease contract before the contract expires and avoid paying a penalty.

## Before you begin

Role required: itil, contract\_manager, inventory\_admin, or ham\_admin,

## About this task

After you choose to extend the lease contract of your asset, various Contract Asset tasks are created to take care of the contract extension process. Close each task to go to the next task and to complete the process.

**Note:** To close the Extension tasks, the Purchase order that is created for the leased asset must be approved by the Procurement manager.

## Procedure

1.  Navigate to **All** &gt; **Contract** &gt; **Contracts** &gt; **Leases**.

2.  Under the Related Links section, click the Leased Assets related list.

3.  Open an asset.

4.  Under the **Contract Asset Tasks** tab, open the Planning task.

5.  Select **Extension** from the Lease action list.

6.  Change the **State** field to **Closed Complete**.

    To take a lease action, you can follow any of the ways mentioned in [Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md).

    The Purchase order and Purchase order lines are created. The **PO Type** field on the Purchase order line is automatically set to **Extension**. You can order the Purchase orders only after completing all the asset tasks that are associated with the items of the Purchase Order line.

    After the Purchase orders are created, Expense lines are created to track the costs of the contract extension.

    An Extension task is created to take care of the extension process.

7.  Under the **Contract Asset Tasks** related list, open the Extension task.

8.  Under the **Extension details** tab, update the **Extension start date** and **Extension end date** fields.

9.  Update the **Extension cost** field with the amount to extend the lease agreement of the asset covered.

    The Purchase order line is automatically updated with the same amount.

10. Change the **State** field to **Closed Complete**.

    An Extension Confirmation task is created to take care of the confirmation process.

11. Under the **Contract Asset Tasks** related list, open the Extension Confirmation task.

    If you want to change the Extension amount from the Extension Confirmation task, then you can change the amount from the Purchase order.

    **Note:** To close the Extension Confirmation task, the Purchase order must be in the Received state.

12. Set the **Extension confirmation** field to **Yes**.

13. Change the **State** field to **Closed Complete**.


## Result

A new contract is created with the start and end dates set as the extension start and end dates.

**Parent Topic:**[Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md)

