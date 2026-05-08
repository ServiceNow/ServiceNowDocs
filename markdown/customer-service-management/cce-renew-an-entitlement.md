---
title: Renew an entitlement
description: Renew an entitlement on the CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Renew an entitlement

Renew an entitlement on the CSM Configurable Workspace.

## Before you begin

You cannot renew an entitlement when it is in Canceled state or it does not have an end date. For more info, see Order fulfillment.

The order processing for product inventory based entitlements are executed according to the fulfillment flow defined by the customer for these offerings being renewed.

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote or opportunity, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the entitlement belongs to.

4.  In the entitlements related list, select the entitlement that you want to renew.

5.  Select **Renew**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to renew the entitlement is created. You can select the quote number from the confirmation message to review the renewal quote. After the quote is approved and the status is updated to **Complete**, an order is created for further processing.
    -   If the selected target entity is an order, an order to renew the entitlement is created. You can select the order number from the confirmation message to review the renewal order.
    -   If the selected target entity is an opportunity, an opportunity to renew the entitlement is created. You can select the opportunity number from the confirmation message to review the renewal opportunity.
    -   If the selected target entity is an opportunity and a quote, both opportunity and quote to renew the entitlement are created. You can navigate to the opportunity and quote by selecting the numbers from the confirmation message.
6.  After the order line items are fulfilled, set the status to **Completed**.

    A new entitlement is created.


## Result

The new entitlement is created in the Draft state. You can see more details in the Renewal History related list.

