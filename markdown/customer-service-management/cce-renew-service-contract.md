---
title: Renew a service contract
description: Renew a service contract and its hierarchy on the CSM Configurable Workspace to renew the services before the service contract expires.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Renew a service contract

Renew a service contract and its hierarchy on the CSM Configurable Workspace to renew the services before the service contract expires.

## Before you begin

You can renew a service contract when it is in Active or Expired state and has an end date.

**Note:** You cannot renew service contracts for product inventory records.

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  Select **Renew**.

5.  In the Renew service contract window, in the **Renew start date** and **Renew end date** fields, enter the start date for the activation of the service contract and the end date for ending the service contract.

6.  Add a reason for a renewing the service contract in the **Reason for renewal** field.

7.  Select **Renew**.

    An order or a quote is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to renew the service contract is created. You can select the quote number from the confirmation message to view the renewed quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to renew the service contract is created. You can select the order number from the confirmation message to view the renewed order line items.
8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    A new service contract is created.


## Result

A new service contract is created in the Draft state. You can see more details in the Renewal History related list.

