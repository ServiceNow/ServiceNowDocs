---
title: Add contract lines to a service contract
description: Add one or more contract lines to a service contract on the CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/cce-add-contract-lines.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Add contract lines to a service contract

Add one or more contract lines to a service contract on the CSM Configurable Workspace.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract to add more contract lines.

4.  On the Service Contract form, select **New**.

    The target entity is created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-cont-ent-workflows-csm.md).

    -   If the selected target entity is a quote, a quote to create new service contract line is created.
    -   If the selected target entity is an order, an order to create new service contract line is created.
    -   If the selected target entity is an opportunity, an opportunity to create a new service contract line is created.
    -   If the selected target entity is an opportunity and a quote, both opportunity and quote to create the service contract are created. You can navigate to the opportunity and quote by selecting the numbers from the confirmation message.
    The Existing contract field will refer the current service contract. All the other fields like Contract start date, Contract end date, and contract renewal fields will be auto-populated with the current contract details.

5.  In the Catalog tab, add products to the new quote or order that is created.

    For more info, see [Add products to a quote](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/sales-and-order-management/quote-management-catalog-tab.md).

6.  Select **Submit for approval**.

7.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    On the Service Contract Line related list, a new service contract line is created and added.


## Result

The new service contract line is added to the contract and is visible on the selected target entity.

