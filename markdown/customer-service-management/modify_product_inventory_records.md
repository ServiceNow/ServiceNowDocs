---
title: Modify product inventory records
description: Perform the Modify operation on a single product inventory record that results in the creation of an order on the CSM Configurable Workspace to update its existing configurations. For example, you may want to add or delete an optional product inventory or update its configurations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Product inventory configurations, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Modify product inventory records

Perform the **Modify**operation on a single product inventory record that results in the creation of an order on the CSM Configurable Workspace to update its existing configurations. For example, you may want to add or delete an optional product inventory or update its configurations.

## Before you begin

Role required: Sales Agent \(sn\_sales\_common.sales\_agent\) or Sales Manager \(sn\_sales\_common.sales\_manager\)

## About this task

When a **Modify** action is performed and an order is created, the fulfillment process for the order begins. After the fulfillment flow is complete, the order is marked as **Complete**and the product inventory record is updated.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the product inventory belongs to.

4.  Navigate to the Product Inventories related list.

    **Note:** The Product Inventories related list will be available out of the box starting from the Yokohama release. Customers using the Washington or Xanadu versions must add the related list manually.

    You can retain either the sold product or the product inventories related list. If you want to retain both the lists, filter out the product inventory records from the sold product related list and perform the **Modify**flow from the product inventory record.

5.  Select a product inventory record in **Active** state and select **Modify**.

    **Note:** The **Modify** flow can be triggered only on a root product inventory record.

6.  On the Configurator UI, modify the existing configurations for the product inventory record.

    To learn more about the Configurator UI, see [Exploring Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-exploring.md).

7.  Select **Update**.

    An order to modify the product inventory is created. You can select the order number from the confirmation message on the account page to open the order and see the order line items. Alternatively, you can find the order in the Customer Orders list.


