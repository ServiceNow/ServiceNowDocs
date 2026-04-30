---
title: Modify a service contract line
description: Modify a service contract line so that you can update its existing configurations.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Modify a service contract line

Modify a service contract line so that you can update its existing configurations.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  In the service contract lines related list, select one ore more service contract line that you want to modify the characteristics and line items for.

5.  Select **Modify** to modify the selected service contract lines.

6.  On the Configurator UI, modify the existing configurations for the service contract line.

    To learn more about the Configurator UI, see [Exploring Sales Customer Relationship Management](../../tmt-order-mgt/concept/som-exploring.md).

    **Note:** The Configurator UI is displayed only if you select a single service contract line. If you selected multiple service contract lines, the order or quote created is displayed.

7.  Select **Update**.

    An order or a quote will be created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to modify the service contract line is created. You can click the quote number from the confirmation message to view the modified quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to modify the service contract line is created. You can click the order number from the confirmation message to view the modified order line items.
8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract line.


**Parent Topic:**[Using Contracts and Entitlements Workflows](../concept/using-customer-cnt-ent-wf.md)

