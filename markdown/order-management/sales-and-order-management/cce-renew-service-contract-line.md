---
title: Renew a customer contract line
description: Renew a customer contract line on the CSM Configurable Workspace. You can renew the services specified in the customer contract line and its associated child customer contract lines and entitlements.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Renew, Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales and Order Management]
---

# Renew a customer contract line

Renew a customer contract line on the CSM Configurable Workspace. You can renew the services specified in the customer contract line and its associated child customer contract lines and entitlements.

## About this task

You cannot renew a customer contract line when it is in Canceled state or it does not have an end date.

The order processing for product inventory based contract lines are executed according to the fulfillment flow defined by the customer for these offerings being renewed.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote or opportunity, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, navigate to **Contracts and Entitlements** &gt; **Customer Contracts**.

3.  In the customer contract lists, select the customer contract that you want to renew.

4.  In the customer contract lines related list, select the customer contract lines that you want to renew.

5.  Select **Renew**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to renew the customer contract line is created. You can select the quote number from the confirmation message to review the renewal quote. After the quote is approved and the status is updated to **Complete**, an order is created for further processing.
    -   If the selected target entity is an order, an order to renew the customer contract line is created. You can select the order number from the confirmation message to review the renewal order.
    -   If the selected target entity is an opportunity, an opportunity to renew the customer contract is created. You can select the opportunity number from the confirmation message to review the renewal opportunity.
    -   If the selected target entity is an opportunity and a quote, both opportunity and quote to renew the customer contract are created. You can navigate to the opportunity and quote by selecting the numbers from the confirmation message.

        **Note:** If you select a quote or an opportunity, the line items with same product offerings and configuration will be consolidated into a single quote or opportunity line. The consolidated line item reflects the total quantity of all the combined items. For more info, see [Consolidate quotes](../../tmt-order-mgt/task/consolidate-quotes.md).

    If more than 20 contract lines are renewed, the target entities are created asynchronously. You can configure the threshold value for the number of contract lines.

6.  Perform an early or late renewal on the customer contract line.

    In early renewal, users can terminate the contract before the expiry date and create a new contract with the desired start date. For late renewal, users can renew expired contracts that are not renewed.

    -   Select a date before the contract expiry date in the **Renew from** field to perform an early renewal. Two quote or order line items are created. One change order or quote line is created with the modified expiry date of the current service contract line. A new renewal quote or order line is created is created with the new start date.
    -   For an expired contract line, enter a new date to renew the service contract line in the **Start from** field. A new renewal quote or order line is created with a new start date.
7.  After the order line items are fulfilled, set the status to **Completed**.

    A new customer contract line is created.


## Result

The new customer contract line is created with the renewed contract line in the Draft state. You can see more details in the Renewal History related list.

