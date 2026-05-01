---
title: Modify a sold product to create a quote
description: Modify a sold product and its complete hierarchy on the CSM Configurable Workspace to generate a quote for any updated characteristics or configurations. For example, a customer may want to find the price to modify a sold product's characteristics and the line items \(hierarchy\) that are associated with it.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Modify a sold product and hierarchy, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Modify a sold product to create a quote

Modify a sold product and its complete hierarchy on the CSM Configurable Workspace to generate a quote for any updated characteristics or configurations. For example, a customer may want to find the price to modify a sold product's characteristics and the line items \(hierarchy\) that are associated with it.

## About this task

Change a sold product or its characteristics. When you modify a sold product's characteristics, a sold product to quote flow is triggered. This flow applies changes to the existing sold product characteristics and presents customers with a quotation based on their selected changes.

Required plugins: Product Configurator UI \(com.sn\_prd\_config\_ui\), Quote Management \(app-l2c-quote-mgmt\), and Customer Lifecycle Management workflows \(com.snc.customer\_lifecycle\_mgmt\_workflows\) \(

Role required: Sales Agent \(sn\_sales\_common.sales\_agent\) and Sales Manager \(sn\_sales\_common.sales\_manager\)

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold product belongs to.

4.  In the Sold products related list, select the product that you want to modify the characteristics and line items for.

5.  Select **Modify** to update the characteristics of the sold product.

    **Note:** If you have both the Order Management \(com.sn\_ind\_tmt\_orm\) and Quote Management \(app-l2c-quote-mgmt\)\) plugins the order agent, order admin, sales agent, and sales manager can perform the **Modify** action that results in an order. To specifically create a quote, customers must configure the decision table to modify existing sold product according to their business needs. Users performing the modify flow must have both the sales agenda and the order agent roles. To learn more about the decision table, see [Modify decision table rules in Workflow Studio](https://www.servicenow.com/docs/access?context=modify-decision-table-rules&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

6.  On the Configurator UI, modify the existing configurations for the sold product.

    To learn more about the Configurator UI, see [Exploring Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=som-exploring&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

7.  Select **Update**.

    A quote to modify the sold product and its hierarchy is created. You can select the quote number from the confirmation message on the sold products page to open the quote and see the quote line items.

    In the Sold product to Quote flow, the data from **Account**, **Contact**, **Name**,**Product Offering**, **Quantity**, **Sys\_id**, **Characteristic**, **Characteristic Option**, and **Characteristic Value** fields are transferred from the Sold Product to Quote Line Item records.


