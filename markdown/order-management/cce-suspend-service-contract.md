---
title: Suspend a customer contract
description: Suspend a customer contract and its child customer contract lines by creating an order on the CSM Configurable Workspace. Suspending a customer contract suspends or disables the services specified in that customer contract.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Suspend, Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Suspend a customer contract

Suspend a customer contract and its child customer contract lines by creating an order on the CSM Configurable Workspace. Suspending a customer contract suspends or disables the services specified in that customer contract.

## Before you begin

You can suspend a customer contract when at least one of the associated root sold products is in Active state. For product inventory records, you can suspend a customer contract when the associated product inventory record is in Active state.

**Note:** If you don’t create a resume order, the customer contract is indefinitely suspended.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  Select **Suspend**.

5.  In the Suspend customer contract window, enter the period of suspension for the customer contract in the **Start date and time** and **End date and time** fields.

    **Note:** If you do not enter a value in the **End date and time** field, the customer contract is suspended indefinitely. You can resume the customer contract manually. For more info, see [Resume a customer contract](cce-resume-service-contract.md).

6.  Add a reason for a suspension in the **Reason for suspension** field.

7.  Select **Suspend**.

    An order with the suspend action is created for that customer contract.

8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract.


## Result

With the customer contract, all the associated customer contract lines and entitlements are also suspended. However, the customer contract stays in the current state. If you specify an end date and time, a resume order line item is created as a part of the same order. After this period of suspension, the customer contract and all its associated child customer contract lines and entitlement will be in Active or Draft state again. After the end date of the customer contract, the suspended customer contract and all its associated child customer contract lines and entitlement move to Expired state.

