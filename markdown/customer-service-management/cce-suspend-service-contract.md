---
title: Suspend a service contract
description: Suspend a service contract and its child service contract lines by creating an order on the CSM Configurable Workspace. Suspending a service contract suspends or disables the services specified in that service contract.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Suspend a service contract

Suspend a service contract and its child service contract lines by creating an order on the CSM Configurable Workspace. Suspending a service contract suspends or disables the services specified in that service contract.

## Before you begin

You can suspend a service contract when at least one of the associated root sold products is in Active state. For product inventory records, you can suspend a service contract when the associated product inventory record is in Active state.

**Note:** If you don’t create a resume order, the service contract is indefinitely suspended.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  Select **Suspend**.

5.  In the Suspend service contract window, enter the period of suspension for the service contract in the **Start date and time** and **End date and time** fields.

    **Note:** If you do not enter a value in the **End date and time** field, the service contract is suspended indefinitely. You can resume the service contract manually. For more info, see [Resume a service contract](cce-resume-service-contract.md).

6.  Add a reason for a suspension in the **Reason for suspension** field.

7.  Select **Suspend**.

    An order with the suspend action is created for that service contract.

8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract.


## Result

With the service contract, all the associated service contract lines and entitlements are also suspended. However, the service contract stays in the current state. If you specify an end date and time, a resume order line item is created as a part of the same order. After this period of suspension, the service contract and all its associated child service contract lines and entitlement will be in Active or Draft state again. After the end date of the service contract, the suspended service contract and all its associated child service contract lines and entitlement move to Expired state.

