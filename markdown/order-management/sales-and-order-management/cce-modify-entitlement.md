---
title: Modify an entitlement
description: Modify an entitlement associated to an account so that you can update its existing configurations.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Modify an entitlement

Modify an entitlement associated to an account so that you can update its existing configurations.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the entitlement belongs to.

4.  In the entitlements related list, select the entitlement that you want to modify the characteristics for.

5.  Select **Modify**.

    **Note:** You can only modify entitlements associated with an account. You cannot modify entitlements associated to service contract lines.

6.  On the Configurator UI, modify the existing configurations for the selected entitlement.

    To learn more about the Configurator UI, see [Exploring Sales Customer Relationship Management](../../tmt-order-mgt/concept/som-exploring.md).

7.  Select **Update**.

    An order or a quote will be created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to modify the entitlement is created. You can click the quote number from the confirmation message to view the modified quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to modify the entitlement is created. You can click the order number from the confirmation message to view the modified order line items.
8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the entitlement.


**Parent Topic:**[Using Contracts and Entitlements Workflows](../concept/using-customer-cnt-ent-wf.md)

