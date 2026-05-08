---
title: Modify a sold product and hierarchy
description: Modify a sold product and its complete hierarchy on the CSM Configurable Workspace so that you can update its existing configurations. For example, you may want to modify a sold product's characteristics and the line items \(hierarchy\) that are associated with it.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Modify a sold product and hierarchy

Modify a sold product and its complete hierarchy on the CSM Configurable Workspace so that you can update its existing configurations. For example, you may want to modify a sold product's characteristics and the line items \(hierarchy\) that are associated with it.

## About this task

After an order is created, the fulfillment process for the order begins. After the order is fulfilled and marked **Complete**, the order to sold product flow is triggered. This flow applies the changes to the sold products. The changes are based on the updates that are specified on the order.

## Before you begin

Required plugins: Product Configurator UI \(app-prd-config-ui\)

Role required: sn\_ind\_tmt\_orm.order\_admin or sn\_ind\_tmt\_orm.order\_agent

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold product belongs to.

4.  In the Sold Products related list, select the product that you want to modify the characteristics and line items for.

    **Note:** You can do a **Modify** action on either the root or the child sold products only if the sold product is in the **Active** state. The sold product must have a product offering without a specification that is associated with it. If you select two sold products at the same time, you can't do the **Modify** action.

5.  Select **Modify**.

6.  On the Configurator UI, modify the existing configurations for the sold product.

    To learn more about the Configurator UI, see Exploring Sales Customer Relationship Management.

7.  Select **Update**.

    An order to modify the sold product is created. You can select the order number from the confirmation message on the sold products page to open the order and see the order line items. Alternatively, you can find the order in the Customer Orders list.


