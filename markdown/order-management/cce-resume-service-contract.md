---
title: Resume a customer contract
description: Resume a customer contract and its child customer contract lines by creating an order on the CSM Configurable Workspace. By resuming a customer contract, you are restarting the services specified in that customer contract.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resume, Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Resume a customer contract

Resume a customer contract and its child customer contract lines by creating an order on the CSM Configurable Workspace. By resuming a customer contract, you are restarting the services specified in that customer contract.

## Before you begin

You can resume a customer contract when at least one of the associated root sold product is in Inactive, Canceled, or Suspended state. For product inventory records, you can resume a customer contract when the associated product inventory record is in Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  Select **Resume**.

5.  In the Resume customer contract window, in the **Start date and time** field, enter when you want to resume the customer contract.

6.  Add a reason for a resuming the customer contract in the **Reason for resumption** field.

7.  Select **Resume**.

    An order for resuming the customer contract is created.

8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract.


## Result

The customer contract and all its associated child contract lines and entitlements are back in Active or Draft state, depending on the start date of the respective entity.

