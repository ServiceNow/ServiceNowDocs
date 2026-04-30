---
title: Cancel an entitlement
description: Cancel an entitlement by creating an order on the CSM Configurable Workspace. By canceling an entitlement, you are canceling or disabling the services and characteristics associated with that entitlement.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Cancel an entitlement

Cancel an entitlement by creating an order on the CSM Configurable Workspace. By canceling an entitlement, you are canceling or disabling the services and characteristics associated with that entitlement.

## Before you begin

You can cancel an entitlement when the associated root sold product is in Active or Suspended state. For product inventory records, you can cancel an entitlement when the associated product inventory record is in Active or Suspended state.

**Note:** You can only cancel entitlements associated with an account. You cannot cancel entitlements associated to service contract lines.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the entitlement belongs to.

4.  In the entitlements related list, select the entitlement that you want to cancel.

5.  Select **Cancel**.

6.  In the Cancel entitlement window, in the **Start date and time** field, enter the date when the entitlement will be disabled.

7.  Add a reason for a cancellation in the **Reason for cancellation** field.

8.  Select **Cancel**.

    An order with the cancel action is created for that entitlement.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the entitlement.


## Result

The entitlement is permanently cancelled and will move to Cancelled state.

**Parent Topic:**[Using Contracts and Entitlements Workflows](../concept/using-customer-cnt-ent-wf.md)

