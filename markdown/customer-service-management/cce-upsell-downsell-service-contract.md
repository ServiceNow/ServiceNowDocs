---
title: Upsell or Downsell a customer contract line
description: Upsell or downsell a customer contract line on the CSM Configurable Workspace. You can reduce or increase the quantities of the products specified in the customer contract line.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Upsell or Downsell a customer contract line

Upsell or downsell a customer contract line on the CSM Configurable Workspace. You can reduce or increase the quantities of the products specified in the customer contract line.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, navigate to **Contracts and Entitlements** &gt; **Customer Contracts**.

3.  In the customer contract lists, select the customer contract that you want to update.

4.  In the customer contract lines related list, select one or more customer contract lines that you want to modify.

5.  From the **Modify entire line** list, select **Modify quantity**.

6.  In the Modify quantity dialog box, you can swap the values fully or partially in the **Quantity** field for both the contract lines.![Modify quantity dialog box](../images/modify-quantity.png)

    For example, if one product has a quantity of 100 and another has 30, you can perform either a full swap or a partial swap. In the screenshot above, a full swap is completed by updating the Quantity field of the first contract line to **130** \(adding the 30 units from the second line\) and setting the second contract line’s quantity to 0. The Change field reflects the change in quantity.

    You can also perform a partial swap. For instance, you can update the second contract line from 30 to 20, and add the remaining 10 units to the first contract line, increasing it from 100 to 110.

7.  Select the start date of the new customer contract line from the **Effective from** field.

8.  Select **Modify**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   In case of a partial swap, three quote lines are created. You can select the quote number from the confirmation message to view the quote line items. The quote is approved and the status changes to **Complete** to create an order with three order line items.
    -   In case of a full swap, two quote lines are created. You can select the quote number from the confirmation message to view the quote line items. The quote is approved and the status changes to **Complete** to create an order with two order line items.
9.  In the Line Items related list, select the State value of the parent order lines and set them to **Completed**.

    In case of partial swap, two new customer contract lines with the modified quantities are created with the Start date as the **Effective from** date. The end date of the existing contract line is updated. In case of full swap, one new customer contract line with the modified quantity is created with the Start date as the **Effective from** date. The end date of the existing contract line is updated.

    **Note:** You can perform a partial or a full swap with a new product from the catalog by following the same procedure.


