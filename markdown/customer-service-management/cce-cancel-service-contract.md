---
title: Cancel a service contract
description: Create an order to cancel a service contract and its child service contract lines on the CSM Configurable Workspace. By canceling a service contract, you are terminating the services specified in that service contract.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Cancel a service contract

Create an order to cancel a service contract and its child service contract lines on the CSM Configurable Workspace. By canceling a service contract, you are terminating the services specified in that service contract.

## Before you begin

You can cancel a service contract when at least one of the associated root sold product is in Active or Suspended state. For product inventory records, you can cancel a service contract when the associated product inventory record is in Active or Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  Select **Cancel**.

    All the associated service contract lines and entitlements will also be cancelled and will be set to the Cancelled state.

5.  In the Cancel service contract window, in the **Start date and time** field, enter the date when the service contract will be cancelled.

6.  Add a reason for a cancellation in the **Reason for cancellation** field.

7.  Select **Cancel**.

    An order with the cancel action is created for that service contract.

8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract.


## Result

With the service contract, all the associated service contract lines and entitlements are also cancelled and will be in **Cancelled** state.

