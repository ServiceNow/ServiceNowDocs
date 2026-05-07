---
title: Submit a request for quote from the Business Portal
description: Browse products and submit a request for quote \(RFQ\) based on your budget and pricing preferences for those products directly through the Business Portal, eliminating the need to engage a sales agent.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Business Portal, Use, Sales Customer Relationship Management]
---

# Submit a request for quote from the Business Portal

Browse products and submit a request for quote \(RFQ\) based on your budget and pricing preferences for those products directly through the Business Portal, eliminating the need to engage a sales agent.

## Before you begin

Role required: sn\_customerservice.customer

## Procedure

1.  Log in to the Business Portal.

2.  Browse the product catalog, select products, and add them to the cart.

    1.  Select **Product Catalog**.

        If you are a contact of an account with an active sales agreement, only the products listed in the sales agreement are displayed.

    2.  Browse the products in the catalog.

    3.  If a product you want to order has specific configurations, select **Customize** and select the product options.

    4.  In the **Quantity** field, enter the quantity of the item you want to order.

    5.  Select **Add** to add products to the cart.

3.  Review the cart contents.

    1.  Select the Cart icon ![](../image/icon-shopping-cart-1.png).

        The information listed in the following table is displayed.

        |Field|Description|
        |-----|-----------|
        |Number|Unique cart ID.|
        |State|State of the cart. For more information, see [Request for quote \(RFQ\) states](../reference/rfq-states.md).|
        |Created|Cart creation timestamp.|
        |Qty|Product quantity.|
        |Unit list price|Price of a single unit of product or service before adjustments.|
        |Cumulative monthly price|Total cost of a product and its child items, if any, over a month.|
        |Cumulative one time price|One-time price of the product and its child items, if any.|

    2.  If you need to modify the quantity or customization for a product in the cart, select the Edit icon ![](../../../reuse/icons/product-icons/pencil-outline-24.svg) and modify the details.

    3.  If you want to delete an item, select the Delete icon ![](../../../common/image/Form_DeleteIcon.png).

4.  Create the Request for quote.

    1.  Select **Request for quote**.

        A request for quote record is created in the Draft state starting with the prefix RFQ.

    2.  On the Details form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Quote required by|Date and time by which you require the quote from the seller.|
        |Overall budget|Allocated spend capacity for purchasing the selected products in US dollars \(USD\).|
        |Short description|Note to the seller about your quote request.|

    3.  Select **Continue**.

    4.  On the Selected products page, review the products that you've added to the quote request.

    5.  Specify a cumulative target price to propose the total amount you'd like to pay for each top-level product.

        1.  Select the Edit icon![](../../../reuse/icons/product-icons/pencil-outline-24.svg).
        2.  In the **Cumulative target price** field, enter a value.
        3.  Select **Update**.
5.  Verify the details on the Review page.

6.  Select **Submit**.


## Result

The state of the quote request changes to Submitted.

The RFQ is submitted for further processing and you're redirected to the Request for quotes details page that displays the list of your submitted quote requests.

## What to do next

View the quote details on the Business Portal after the sales agent reviews and generates a quote for your request. For more information, see [View requests for quotes \(RFQs\) on the Business Portal](view-rfq-business-portal.md).

**Related topics**  


[View quotes from the Business Portal](view-quotes-business-portal.md)

