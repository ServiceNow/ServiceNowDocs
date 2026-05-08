---
title: Modify product inventory records to create a quote
description: Perform the Modify operation on a single product inventory record that results in the creation of a quote on the CSM Configurable Workspace. For example, you might want to add or delete an optional product inventory or update its configurations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Modify product inventory records, Product inventory configurations, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Modify product inventory records to create a quote

Perform the **Modify**operation on a single product inventory record that results in the creation of a quote on the CSM Configurable Workspace. For example, you might want to add or delete an optional product inventory or update its configurations.

## Before you begin

Role required: Order admin \(sn\_ind\_tmt\_orm.order\_admin\) or Order agent \(sn\_ind\_tmt\_orm.order\_agent\)

## About this task

The **Modify** flow generates a quote. After the quote is marked as **Complete**, an order is created. On fulfillment of the order, the product inventory record is updated.

Required plugins: Product Configurator UI \(com.sn\_prd\_config\_ui\), Quote Management \(app-l2c-quote-mgmt\), and Customer Lifecycle Management workflows \(com.snc.customer\_lifecycle\_mgmt\_workflows\)

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the product inventory belongs to.

4.  Navigate to the **Product Inventories** related list.

5.  Select a single product inventory record in **Active** state and select **Modify**.

    **Note:** The **Modify** flow can be triggered only on a root product inventory record.

    If you have both the Order Management \(com.sn\_ind\_tmt\_orm\) and Quote Management \(app-l2c-quote-mgmt\)\) plugins the order agent, order admin, sales agent, and sales manager can perform the Modify action that results in an order. Users performing the modify flow must have both the sales agent and the order agent roles. To specifically create a quote, customers must configure the decision table to modify existing sold product according to their business needs. Update the configurations on the Customer Life Cycle Workflows policy decision table. To learn more about the decision table, see [Modify decision table rules in Workflow Studio](https://www.servicenow.com/docs/access?context=modify-decision-table-rules&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

6.  On the Configurator UI, modify the existing configurations for the product inventory.

    To learn more about the Configurator UI, see [Exploring Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=som-exploring&version=australia&pubname=australia-order-management&ft:locale=en-US).

    A quote to modify the product inventory is created. You can select the quote number from the confirmation message on the account page to open the quote and see the quote line items. Alternatively, you can find the quote from **All Menu** &gt; **Quote** in the Quote list.


