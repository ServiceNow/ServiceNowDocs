---
title: Modify a customer contract line
description: Modify a customer contract line so that you can update its existing configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/cce-modify-service-contract-line.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Modify, Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Modify a customer contract line

Modify a customer contract line so that you can update its existing configurations.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract.

4.  In the customer contract lines related list, select one or more customer contract lines that you want to modify.

5.  From the **Modify** list, select one of the options to perform one of these actions:

    -   If you select **Modify entire line**, the Configurator UI is displayed. Modify the existing configurations for the customer contract line.

        **Note:** The Configurator UI is displayed only if you select a single customer contract line. If you selected multiple customer contract lines, the order or quote created is displayed.

    -   If you select **Modify quantity**, you can reduce or increase the quantities of the products specified in the selected contract lines. For more info, see [Upsell or Downsell a customer contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/cce-upsell-downsell-service-contract.md).

        **Note:** You cannot modify quantity on a ramped contract line.

    -   If you select **Modify end date**, you can select an earlier end date or a later end date than the current end date to perform an early termination or extension of a contract line. For a ramped contract line, you can only select a date before the contract expiry date in the **End date** field to perform an early termination. The contract line splits into two contract lines. One contract line has the new end date that you selected and the second contract line has the original end date with State as **Canceled** and Quantity as **Zero**. The remaining segments are canceled and their quantities are zero.
6.  Select **Update**.

    An order or a quote is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/create-cont-ent-workflows-csm.md).

    -   If the selected target entity is a quote, a quote to modify the customer contract line is created. You can select the quote number from the confirmation message to view the modified quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to modify the customer contract line is created. You can select the order number from the confirmation message to view the modified order line items.
7.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the customer contract line.


