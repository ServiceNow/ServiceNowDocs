---
title: Cancel a service contract line
description: Create an order to cancel a service contract line and its child service contract lines on the CSM Configurable Workspace. By canceling a service contract line, you are canceling or disabling the services and characteristics associated with that service contract line.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Cancel a service contract line

Create an order to cancel a service contract line and its child service contract lines on the CSM Configurable Workspace. By canceling a service contract line, you are canceling or disabling the services and characteristics associated with that service contract line.

## Before you begin

You can cancel a service contract line when the associated root sold product is in Active or Suspended state. For product inventory records, you can cancel a service contract line when the associated product inventory record is in Active or Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  In the service contract, select the service contract line from the service contract lines related list, that you want to cancel.

5.  Select **Cancel**.

6.  In the Cancel service contract line window, in the **Start date and time** field, enter the date when the service contract line will be disabled.

7.  Add a reason for a cancellation in the **Reason for cancellation** field.

8.  Select **Cancel**.

    An order with the cancel action is created for that service contract line.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract line.


## Result

With the service contract line, all the associated entities in the hierarchy are also cancelled and move to Cancelled state.

