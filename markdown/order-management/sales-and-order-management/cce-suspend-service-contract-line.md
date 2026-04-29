---
title: Suspend a customer contract line
description: Suspend a customer contract line and its child customer contract lines by creating an order on the CSM Configurable Workspace. By suspending a customer contract line, you are suspending or disabling the services and characteristics associated with that customer contract line.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Suspend, Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales and Order Management]
---

# Suspend a customer contract line

Suspend a customer contract line and its child customer contract lines by creating an order on the CSM Configurable Workspace. By suspending a customer contract line, you are suspending or disabling the services and characteristics associated with that customer contract line.

## About this task

## Before you begin

You can suspend a customer contract line when the associated root sold product is in Active state. For product inventory records, you can suspend a customer contract line when the associated product inventory record is in Active state.

**Note:** If you don’t create a resume order, the customer contract line is indefinitely suspended.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  Select the customer contract line from the customer contract lines related list, that you want to suspend.

5.  Select **Suspend**.

6.  In the Suspend customer contract line window, enter the period of suspension for the customer contract line in the **Start date and time** and the **End date and time** field.

    **Note:** If you do not enter a value in the **End date and time**, the customer contract line will be suspended. You can manually resume the customer contract by using the resume option. For more info, see [Resume a customer contract line](cce-resume-service-contract-line.md)

7.  Add a reason for a suspension in the **Reason for suspension** field.

8.  Select **Suspend**.

    An order with the suspend action is created for that customer contract line.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract line.


## Result

With the customer contract line, all the associated entities in the hierarchy are also suspended. If you specify an end date and time, a resume order line item is created as a part of the same order. After this period of suspension, the customer contract line will be in Active state again. After the end date of the customer contract, the suspended customer contract line and all its associated child customer contract lines and entitlement move to Expired state.

