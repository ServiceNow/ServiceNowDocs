---
title: Update product locations at the order line level
description: Agents can use the copy function to update product locations at the order line level Order Management.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an order in Order Management, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Update product locations at the order line level

Agents can use the copy function to update product locations at the order line level Order Management.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

Agents can change the location of products at the order line level by using the copy function. When an order line item is copied, a dialog box opens allowing the agent to select a location. Agents can select one line item to update or multiple line items.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  From the **Customer Orders** &gt; **All**, select the order you want to work with and select the **Line Items** tab.

3.  Select one or more order line items that you want to change to another location.

4.  Select **Copy**.

    ![](../image/som-copy-order-line-location.png)

5.  In the **Copy line items** window, choose any one of the options.

<table id="choicetable_ij4_ykn_zcc"><thead><tr><th align="left" id="d48507e119">

 

</th><th align="left" id="d48507e121">

 

</th></tr></thead><tbody><tr><td id="d48507e126">

**Keep original location**

</td><td>

Line items for the selected quote are created and the source location is retained.

</td></tr><tr><td id="d48507e135">

**Choose new location**

</td><td>

This action copies the quote line items to a new location.In the **Service location** filter, select the new location that you want the line items to be copied to.

</td></tr></tbody>
</table>    **Note:** Be sure to select **Continue to copy only eligible lines for this location \(exclude ineligible\)** within the **Copy line items** window.

    This selection copies the eligible line items to your new location and skips the line items that aren’t eligible. If the option isn’t selected, no quote line items are copied.

6.  Select **Copy**.

    The order lines are copied and added to the order line items list with a new location.


**Parent Topic:**[Create an order in Order Management](som-create-product-order.md)

