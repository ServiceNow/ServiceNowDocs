---
title: Renew a service contract line
description: Renew a service contract line on the CSM Configurable Workspace. You can renew the services specified in the service contract line and its associated child service contract lines and entitlements.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Renew a service contract line

Renew a service contract line on the CSM Configurable Workspace. You can renew the services specified in the service contract line and its associated child service contract lines and entitlements.

## About this task

You cannot renew a service contract line when it is in Canceled state or it does not have an end date.

The order processing for product inventory based contract lines are executed according to the fulfillment flow defined by the customer for these offerings being renewed.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote or opportunity, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the list view, navigate to **Contracts and Entitlements** &gt; **Service Contracts**.

3.  In the service contract lists, select the service contract that you want to renew.

4.  In the service contract lines related list, select the service contract line that you want to resume.

5.  Select **Renew**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to renew the service contract line is created. You can select the quote number from the confirmation message to review the renewal quote. After the quote is approved and the status is updated to **Complete**, an order is created for further processing.
    -   If the selected target entity is an order, an order to renew the service contract line is created. You can select the order number from the confirmation message to review the renewal order.
    -   If the selected target entity is an opportunity, an opportunity to renew the service contract is created. You can select the opportunity number from the confirmation message to review the renewal opportunity.
    -   If the selected target entity is an opportunity and a quote, both opportunity and quote to renew the service contract are created. You can navigate to the opportunity and quote by selecting the numbers from the confirmation message.
6.  After the order line items are fulfilled, set the status to **Completed**.

    A new service contract line is created.


## Result

The new service contract line is created with the renewed contract line in the Draft state. You can see more details in the Renewal History related list.

