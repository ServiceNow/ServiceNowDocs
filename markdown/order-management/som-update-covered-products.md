---
title: Add covered products to order line items
description: Enhance orders by adding covered products such as contracts or entitlements at the order line level.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/order-management/som-update-covered-products.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an order in Order Management, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Add covered products to order line items

Enhance orders by adding covered products such as contracts or entitlements at the order line level.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent or sn\_ind\_tmt\_orm.order\_manager

## About this task

Order agents can add covered products like entitlements or contracts to an order line during the order capture process.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** \[Omitted image "Lists.png"\] Alt text: view.

2.  Navigate to **Customer orders** &gt; **All** and select the order that you’re working with.

3.  From the **Order line items** tab, select the entitlement or contract type of order line.

4.  Select **More** &gt; **Covered product**.

    \[Omitted image "som-covered-product.png"\] Alt text: Image shows how agents can select Covered Products from the more menu in the order line form.

5.  In the Covered Product form, select **New**.

6.  In the Create New Covered Product form, select the covered product line item you want to add.

    There are three types of covered products types that you can add to a line item:

<table id="choicetable_lyy_34l_wbc"><thead><tr><th align="left" id="d43320e136">

Covered product type

</th><th align="left" id="d43320e139">

Description

</th></tr></thead><tbody><tr><td id="d43320e145">

**Covered sold product**

</td><td>

Add a sold product to an entitlement/contract type of order line to establish a coverage relationship between them.

</td></tr><tr><td id="d43320e157">

**Covered order line item**

</td><td>

Add a covered order line item to the order line.

</td></tr><tr><td id="d43320e166">

**Covered install base item**

</td><td>

Add an install base item to the order line.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  On the order line item page, select the contract start date and the contract end date.

9.  Change the state to **Complete**.

    A contract is created with the contract details for the order line.


**Parent Topic:**[Create an order in Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/order-management/som-create-product-order.md)

