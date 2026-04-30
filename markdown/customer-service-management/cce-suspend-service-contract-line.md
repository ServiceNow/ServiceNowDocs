---
title: Suspend a service contract line
description: Suspend a service contract line and its child service contract lines by creating an order on the CSM Configurable Workspace. By suspending a service contract line, you are suspending or disabling the services and characteristics associated with that service contract line.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Suspend a service contract line

Suspend a service contract line and its child service contract lines by creating an order on the CSM Configurable Workspace. By suspending a service contract line, you are suspending or disabling the services and characteristics associated with that service contract line.

## About this task

## Before you begin

You can suspend a service contract line when the associated root sold product is in Active state. For product inventory records, you can suspend a service contract line when the associated product inventory record is in Active state.

**Note:** If you don’t create a resume order, the service contract line is indefinitely suspended.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  Select the service contract line from the service contract lines related list, that you want to suspend.

5.  Select **Suspend**.

6.  In the Suspend service contract line window, enter the period of suspension for the service contract line in the **Start date and time** and the **End date and time** field.

    **Note:** If you do not enter a value in the **End date and time**, the service contract line will be suspended. You can manually resume the service contract by using the resume option. For more info, see [Resume a service contract line](cce-resume-service-contract-line.md)

7.  Add a reason for a suspension in the **Reason for suspension** field.

8.  Select **Suspend**.

    An order with the suspend action is created for that service contract line.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract line.


## Result

With the service contract line, all the associated entities in the hierarchy are also suspended. If you specify an end date and time, a resume order line item is created as a part of the same order. After this period of suspension, the service contract line will be in Active state again. After the end date of the service contract, the suspended service contract line and all its associated child service contract lines and entitlement move to Expired state.

