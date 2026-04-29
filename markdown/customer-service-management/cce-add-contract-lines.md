---
title: Add contract lines to a customer contract
description: Add one or more contract lines to a customer contract on the CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Add contract lines to a customer contract

Add one or more contract lines to a customer contract on the CSM Configurable Workspace.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Customer Contracts**.

3.  In the Contracts and Entitlements - Customer Contracts list, select the customer contract to add more contract lines.

4.  On the Customer Contract form, select **Customer Contract Lines** related list.

5.  Select **New**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](../concept/create-cont-ent-workflows-csm.md#section_qp4_rxv_tcc).

    -   If the selected target entity is a quote, a quote to create new customer contract line is created.
    -   If the selected target entity is an order, an order to create new customer contract line is created.
    -   If the selected target entity is an opportunity, an opportunity to create a new customer contract line is created.
    -   If the selected target entity is an opportunity and a quote, both opportunity and quote to create the customer contract are created. You can navigate to the opportunity and quote by selecting the numbers from the confirmation message.
    The Existing contract field will refer the current customer contract. All the other fields like Contract start date, Contract end date, and contract renewal fields will be auto-populated with the current contract details.

6.  In the Catalog tab, add products to the new quote or order that is created.

    For more info, see [Add products to a quote](https://www.servicenow.com/docs/access?context=quote-management-catalog-tab&version=australia&pubname=australia-order-management&ft:locale=en-US).

7.  Select **Submit for approval**.

8.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    On the Customer Contract Line related list, a new customer contract line is created and added.


## Result

The new customer contract line is added to the contract and is visible on the selected target entity. The new customer contract line is synced with auto-renewal quote or opportunity that is generated for the contract. When the associated customer contract is auto renewed, the new customer contract line is automatically renewed and added to the renewal quote or opportunity.

