---
title: Renew a service contract
description: Renew a service contract on the CSM Configurable Workspace before the service contract expires.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Renew a service contract

Renew a service contract on the CSM Configurable Workspace before the service contract expires.

## Before you begin

You cannot renew a service contract when it is in Canceled state or it does not have an end date.

The order processing for product inventory based contracts are executed according to the fulfillment flow defined by the customer for these offerings being renewed.

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote or opportunity, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  Select **Renew**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to renew the service contract is created. You can select the quote number from the confirmation message to review the renewal quote. After the quote is approved and the status is updated to **Complete**, an order is created for further processing.
    -   If the selected target entity is an order, an order to renew the service contract is created. You can select the order number from the confirmation message to review the renewal order.
    -   If the selected target entity is an opportunity, an opportunity to renew the service contract is created. You can select the opportunity number from the confirmation message to review the renewal opportunity.
    -   If the selected target entity is an opportunity and a quote, both opportunity and quote to renew the service contract are created. You can navigate to the opportunity and quote by selecting the numbers from the confirmation message.
5.  After the order line items are fulfilled, set the status to **Completed**.

    A new service contract is created.


## Result

A new service contract is created in the Draft state. You can view more details in the Renewal History related list.

**Parent Topic:**[Using Contracts and Entitlements Workflows](../concept/using-customer-cnt-ent-wf.md)

