---
title: Resume a service contract
description: Resume a service contract and its child service contract lines by creating an order on the CSM Configurable Workspace. By resuming a service contract, you are restarting the services specified in that service contract.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Resume a service contract

Resume a service contract and its child service contract lines by creating an order on the CSM Configurable Workspace. By resuming a service contract, you are restarting the services specified in that service contract.

## Before you begin

You can resume a service contract when at least one of the associated root sold product is in Inactive, Canceled, or Suspended state. For product inventory records, you can resume a service contract when the associated product inventory record is in Suspended state.

Role required: sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  Select **Resume**.

5.  In the Resume service contract window, in the **Start date and time** field, enter when you want to resume the service contract.

6.  Add a reason for a resuming the service contract in the **Reason for resumption** field.

7.  Select **Resume**.

    An order for resuming the service contract is created.

8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract.


## Result

The service contract and all its associated child contract lines and entitlements are back in Active or Draft state, depending on the start date of the respective entity.

**Parent Topic:**[Using Contracts and Entitlements Workflows](../concept/using-customer-cnt-ent-wf.md)

