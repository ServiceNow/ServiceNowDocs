---
title: Cancel a customer contract line
description: Create an order to cancel a customer contract line and its child customer contract lines on the CSM Configurable Workspace. By canceling a customer contract line, you are canceling or disabling the services and characteristics associated with that customer contract line.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cancel, Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales and Order Management]
---

# Cancel a customer contract line

Create an order to cancel a customer contract line and its child customer contract lines on the CSM Configurable Workspace. By canceling a customer contract line, you are canceling or disabling the services and characteristics associated with that customer contract line.

## Before you begin

You can cancel a customer contract line when the associated root sold product is in Active or Suspended state. For product inventory records, you can cancel a customer contract line when the associated product inventory record is in Active or Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  In the customer contract, select the customer contract line from the customer contract lines related list, that you want to cancel.

5.  Select **Cancel**.

6.  In the Cancel customer contract line window, in the **Start date and time** field, enter the date when the customer contract line will be disabled.

7.  Add a reason for a cancellation in the **Reason for cancellation** field.

8.  Select **Cancel**.

    An order with the cancel action is created for that customer contract line.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract line.


## Result

With the customer contract line, all the associated entities in the hierarchy are also cancelled and move to Cancelled state.

