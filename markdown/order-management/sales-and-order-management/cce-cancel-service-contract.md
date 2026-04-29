---
title: Cancel a customer contract
description: Create an order to cancel a customer contract and its child customer contract lines on the CSM Configurable Workspace. By canceling a customer contract, you are terminating the services specified in that customer contract.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cancel, Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales and Order Management]
---

# Cancel a customer contract

Create an order to cancel a customer contract and its child customer contract lines on the CSM Configurable Workspace. By canceling a customer contract, you are terminating the services specified in that customer contract.

## Before you begin

You can cancel a customer contract when at least one of the associated root sold product is in Active or Suspended state. For product inventory records, you can cancel a customer contract when the associated product inventory record is in Active or Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  Select **Cancel**.

    All the associated customer contract lines and entitlements will also be cancelled and will be set to the Cancelled state.

5.  In the Cancel customer contract window, in the **Start date and time** field, enter the date when the customer contract will be cancelled.

6.  Add a reason for a cancellation in the **Reason for cancellation** field.

7.  Select **Cancel**.

    An order with the cancel action is created for that customer contract.

8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract.


## Result

With the customer contract, all the associated customer contract lines and entitlements are also cancelled and will be in **Cancelled** state.

