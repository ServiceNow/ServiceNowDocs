---
title: Modify a customer contract
description: Modify a customer contract so that you can update its existing configurations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Modify a customer contract

Modify a customer contract so that you can update its existing configurations.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  Select **Modify all lines** to modify the customer contract.

5.  On the Configurator UI, modify the existing configurations for the customer contract line.

    To learn more about the Configurator UI, see [Exploring Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=som-exploring&version=australia&pubname=australia-order-management&ft:locale=en-US).

    **Note:** The Configurator UI is displayed only if the customer contract has a single customer contract line. For multiple customer contract lines, a quote or an order will be created with contract lines in Draft or Active state.

6.  Select **Update**.

    An order or a quote will be created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to modify the customer contract is created. You can select the quote number from the confirmation message to view the modified quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to modify the customer contract is created. You can click the order number from the confirmation message to view the modified order line items.
7.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract.


