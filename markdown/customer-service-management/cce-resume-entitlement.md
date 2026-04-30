---
title: Resume an entitlement
description: Resume an entitlement by creating an order on the CSM Configurable Workspace. By resuming an entitlement, you are restarting the services and the characteristics specified in that entitlement.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Resume an entitlement

Resume an entitlement by creating an order on the CSM Configurable Workspace. By resuming an entitlement, you are restarting the services and the characteristics specified in that entitlement.

## Before you begin

You can resume an entitlement when the associated root sold product is in Inactive, Cancelled, or Suspended state. For product inventory records, you can resume an entitlement when the associated product inventory record is in Suspended state.

**Note:** You can only resume entitlements associated with an account. You cannot resume entitlements associated to service contract lines.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the entitlement belongs to.

4.  In the entitlements related list, select the entitlement that you want to resume.

5.  Select **Resume**.

6.  In the Resume entitlement window, in the **Start date and time** field, enter when you want to resume the entitlement.

7.  Add a reason for a resuming the entitlement in the **Reason for resumption** field.

8.  Select **Resume**.

    An order for resuming the entitlement is created.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the entitlement.


## Result

The entitlement is back in Active or Draft state, based on the start date of the entitlement.

