---
title: Renew a service contract line
description: Renew a service contract line on the CSM Configurable Workspace. You can renew the services specified in the service contract line and its associated child service contract lines and entitlements.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Renew a service contract line

Renew a service contract line on the CSM Configurable Workspace. You can renew the services specified in the service contract line and its associated child service contract lines and entitlements.

## About this task

You can renew a service contract line when it is in Active or Expired state and has an end date.

**Note:** You cannot renew service contract lines for product inventory records.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the list view, navigate to **Contracts and Entitlements** &gt; **Service Contracts**.

3.  In the service contract lists, select the service contract that you want to renew.

4.  In the service contract lines related list, select the service contract line that you want to resume.

5.  Select **Renew**.

6.  In the Renew service contract line window, in the **Renew start date** field, enter the start date for the activation of the service contract line.

7.  Add a reason for a renewing the service contract line in the **Reason for renewal** field.

8.  Select **Renew**.

    An order or a quote is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to renew the service contract line is created. You can select the quote number from the confirmation message to view the renewed quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to renew the service contract line is created. You can select the order number from the confirmation message to view the renewed order line items.
9.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    A new service contract line is created.


## Result

The new service contract line is created with the renewed contract line in the Draft state. You can see more details in the Renewal History related list.

