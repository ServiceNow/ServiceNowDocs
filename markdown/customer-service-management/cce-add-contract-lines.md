---
title: Add contract lines to a service contract
description: Add one or more contract lines to a service contract on the CSM Configurable Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-06-25"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Using Customer Contracts and Entitlements, Customer management, Using Customer Service Management, Customer Service Management]
---

# Add contract lines to a service contract

Add one or more contract lines to a service contract on the CSM Configurable Workspace.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract to add more contract lines.

4.  On the Service Contract form, select **Add Contract Line**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to create new service contract line is created.
    -   If the selected target entity is an order, an order to create new service contract line is created.
    The Existing contract field will refer the current service contract. All the other fields like Contract start date, Contract end date, and contract renewal fields will be auto-populated with the current contract details.

5.  In the Catalog tab, add products to the new quote or order that is created.

    For more info, see [Add products to a quote](https://www.servicenow.com/docs/access?context=quote-management-catalog-tab&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US).

6.  Select **Submit for approval**.

7.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    On the Service Contract Line related list, a new service contract line is created and added.


