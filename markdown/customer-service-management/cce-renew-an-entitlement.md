---
title: Renew an entitlement
description: Renew an entitlement on the CSM Configurable Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Renew an entitlement

Renew an entitlement on the CSM Configurable Workspace.

## Before you begin

You can renew an entitlement when it is in Active or Expired state and has an end date.

**Note:** You cannot renew entitlements for product inventory records.

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the entitlement belongs to.

4.  In the entitlements related list, select the entitlement that you want to renew.

5.  Select **Renew**.

6.  In the Renew entitlement window, in the **Renew start date** field, enter the start date for the activation of the entitlement.

7.  Add a reason for a renewing the entitlement in the **Reason for renewal** field.

8.  Select **Renew**.

    An order or a quote is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to renew the entitlement is created. You can select the quote number from the confirmation message to view the renewed quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to renew the entitlement is created. You can select the order number from the confirmation message to view the renewed order line items.
9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    A new entitlement is created.


## Result

The new entitlement is created in the Draft state. You can see more details in the Renewal History related list.

