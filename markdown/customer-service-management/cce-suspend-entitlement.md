---
title: Suspend an entitlement
description: Suspend an entitlement by creating an order on the CSM Configurable Workspace. By suspending an entitlement, you are suspending or disabling the services and characteristics associated with that entitlement.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Suspend an entitlement

Suspend an entitlement by creating an order on the CSM Configurable Workspace. By suspending an entitlement, you are suspending or disabling the services and characteristics associated with that entitlement.

## Before you begin

You can suspend an entitlement when the associated root sold product is in Active state. For product inventory records, you can suspend an entitlement when the associated product inventory record is in Active state.

**Note:** You can only suspend entitlements associated with an account. You cannot suspend entitlements associated to service contract lines.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the entitlement belongs to.

4.  In the entitlements related list, select the entitlement that you want to suspend.

5.  Select **Suspend**.

6.  In the Suspend entitlement window, enter the period of suspension for the entitlement in the **Start date and time** and the **End date and time** field.

    **Note:** If you do not enter a value in the **End date and time**, the entitlement will be suspended You can resume the entitlement manually by using the resume option. For more info, see [Resume an entitlement](cce-resume-entitlement.md).

7.  Add a reason for a suspension in the **Reason for suspension** field.

8.  Select **Suspend**.

    An order with the suspend action is created for that entitlement.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the entitlement.


## Result

If you specify an end date and time, a resume order line item is created as a part of the same order. After this period of suspension, the entitlement will be in Active state again. After the end date of the entitlement, the suspended entitlement will move to Expired state.

