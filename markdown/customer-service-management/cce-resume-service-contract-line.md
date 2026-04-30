---
title: Resume a service contract line
description: Create an order to resume a service contract line and its child service contract lines on the CSM Configurable Workspace. By resuming a service contract line, you are restarting the services specified in that service contract line.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Resume a service contract line

Create an order to resume a service contract line and its child service contract lines on the CSM Configurable Workspace. By resuming a service contract line, you are restarting the services specified in that service contract line.

## Before you begin

You can resume a service contract line when the associated root sold product is in Inactive, Cancelled, or Suspended state. For product inventory records, you can resume a service contract line when the associated product inventory record is in Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  In the service contract lines related list, select the service contract line that you want to resume.

5.  Select **Resume**.

6.  In the Resume service contract line window, in the **Start date and time** field, enter when you want to resume the service contract line.

7.  Add a reason for a resuming the service contract line in the **Reason for resumption** field.

8.  Select **Resume**.

    An order for resuming the service contract line is created.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract line.


## Result

With the service contract line, all the associated entities in the hierarchy are also back in Active or Draft state, depending on the start date of the respective entity.

