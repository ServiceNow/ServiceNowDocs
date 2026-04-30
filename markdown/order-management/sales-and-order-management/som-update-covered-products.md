---
title: Add covered products to order line items
description: Enhance orders by adding covered products such as contracts or entitlements at the order line level.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Add covered products to order line items

Enhance orders by adding covered products such as contracts or entitlements at the order line level.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent or sn\_ind\_tmt\_orm.order\_manager

## About this task

Order agents can add covered products to an order line during the order capture process. Covered products refer to offerings that act as entitlements or contracts linked to a primary product, such as a warranty purchased with a phone. They are not standalone products but provide additional value or service to the main product. In the product offering record, covered products are marked with Entitlement as the offering type. You can only link the entitlement to a specific product, sold product, or install base item associated with the account.

You can add multiple covered products to an order line item.

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace.** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select the order that you’re working with.

5.  From the **Line items** tab, select the entitlement or contract type of order line to open the order line record in its own tab.

6.  In the Covered Product form, select **New**.

7.  In the Create New Covered Product form, select the covered product line item you want to add.

    You can add either of the following covered products types to a line item:

    -   **Covered sold product**: Add a sold product to an entitlement/contract type of order line to establish a coverage relationship between them.
    -   **Covered order line item**: Add a covered order line item to the order line.
    -   **Covered install base item**: Add an install base item to the order line.
8.  Select **Save**.

    **Note:** You can't modify a covered product added to an order line. To make changes, delete the covered product by selecting **More Actions icon ![](../image/icon-three-dot-menu.png)** &gt; **Delete** and add the covered product again by selecting **New**.

9.  On the order line item page, select the contract start date and the contract end date.

10. Change the state to **Complete**.

    A contract is created with the contract details for the order line.


**Related topics**  


[Add Covered Products using Contracts and Entitlement Workflow](../../post-sales-support/concept/adding-cov-prod-cceworkflows.md)

