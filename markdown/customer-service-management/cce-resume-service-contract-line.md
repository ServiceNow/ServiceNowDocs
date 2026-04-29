---
title: Resume a customer contract line
description: Create an order to resume a customer contract line and its child customer contract lines on the CSM Configurable Workspace. By resuming a customer contract line, you are restarting the services specified in that customer contract line.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Resume a customer contract line

Create an order to resume a customer contract line and its child customer contract lines on the CSM Configurable Workspace. By resuming a customer contract line, you are restarting the services specified in that customer contract line.

## Before you begin

You can resume a customer contract line when the associated root sold product is in Inactive, Cancelled, or Suspended state. For product inventory records, you can resume a customer contract line when the associated product inventory record is in Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  In the customer contract lines related list, select the customer contract line that you want to resume.

5.  Select **Resume**.

6.  In the Resume customer contract line window, in the **Start date and time** field, enter when you want to resume the customer contract line.

7.  Add a reason for a resuming the customer contract line in the **Reason for resumption** field.

8.  Select **Resume**.

    An order for resuming the customer contract line is created.

9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract line.


## Result

With the customer contract line, all the associated entities in the hierarchy are also back in Active or Draft state, depending on the start date of the respective entity.

