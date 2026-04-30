---
title: Upsell or Downsell a service contract line
description: Upsell or downsell a service contract line on the CSM Configurable Workspace. You can reduce or increase the quantities of the products specified in the service contract line.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-06-25"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Upsell or Downsell a service contract line

Upsell or downsell a service contract line on the CSM Configurable Workspace. You can reduce or increase the quantities of the products specified in the service contract line.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the list view, navigate to **Contracts and Entitlements** &gt; **Service Contracts**.

3.  In the service contract lists, select the service contract that you want to update.

4.  In the service contract lines related list, select one or more service contract lines that you want to update.

5.  Select **Upsell or downsell**.

6.  In the Upsell or downsell dialog box, increase or reduce the value in the **Quantity** field.

7.  Select the start date of the new service contract line from the **Effective from** field.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to upsell or downsell the service contract line is created. You can select the quote number from the confirmation message to view the quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to upsell or downsell the service contract line is created. You can select the order number from the confirmation message to view the order line items.
8.  In the Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    A new service contract line with the increased or reduced quantities is created with the Start date as the **Effective from** date you selected.

    **Note:** For upsell, the Start date and End date of the original service contract line unchanged. For downsell, the End date of the original service contract line is updated to n-1 date of Start date of the new service contract line.


