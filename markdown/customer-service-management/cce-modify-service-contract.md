---
title: Modify a service contract
description: Modify a service contract so that you can update its existing configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/cce-modify-service-contract.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Contracts and Entitlements Workflows, Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Modify a service contract

Modify a service contract so that you can update its existing configurations.

## Before you begin

Role required:

-   To create an order, you need sn\_customerservice\_manager and sn\_ind\_tmt\_orm.order\_agent.
-   To create a quote, you need sn\_customerservice\_manager and sn\_sales\_common.sales\_agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the Contracts and Entitlements list, select **Service Contracts**.

3.  In the Contracts and Entitlements - Service Contracts list, select the service contract.

4.  Select **Modify all lines** to modify the service contract.

5.  On the Configurator UI, modify the existing configurations for the service contract line.

    To learn more about the Configurator UI, see .

    **Note:** The Configurator UI is displayed only if the service contract has a single service contract line. For multiple service contract lines, a quote or an order will be created with contract lines in Draft or Active state.

6.  Select **Update**.

    An order or a quote will be created depending on the rules set in the Customer Life Cycle Workflows Policy decision table. For more info, see [Configuring Customer Life Cycle Workflows Policy decision table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-cont-ent-workflows-csm.md).

    -   If the selected target entity is a quote, a quote to modify the service contract is created. You can select the quote number from the confirmation message to view the modified quote line items. The quote is approved and the status changes to **Complete** to create an order.
    -   If the selected target entity is an order, an order to modify the service contract is created. You can click the order number from the confirmation message to view the modified order line items.
7.  In the Order Line Items related list, double-click the State value of the parent order line and set it to **Completed**.

    The modifications are visible on the service contract.


