---
title: Request updates for one or more orders
description: Request changes to the expected order fulfillment date and shipping location for one or more orders or to draw attention to an issue by creating an order case from the Business Portal.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Business Portal, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Request updates for one or more orders

Request changes to the expected order fulfillment date and shipping location for one or more orders or to draw attention to an issue by creating an order case from the Business Portal.

## Before you begin

Role required: sn\_customerservice.customer

## Procedure

1.  Log in to the Business Portal.

2.  Select **Requests** &gt; **Submit a request** &gt; **Submit a case** &gt; **Submit an order case**.

3.  Create a new order case.

    1.  On the form, fill in the fields.

<table id="table_kph_1wl_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

The account for which you’re creating the case.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for this case.

</td></tr><tr><td>

Scope of request

</td><td>

This option should be set to **Order header details, multiple orders** to create a case for one or more orders.

</td></tr><tr><td>

Priority

</td><td>

The available assigned priorities are:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low \(default\)


</td></tr><tr><td>

Short description

</td><td>

Optional brief description.

</td></tr></tbody>
</table>    2.  Select **Next**.

        An order case is created with its State as Draft.

4.  Select the orders that you want to add to the order case.

    1.  On the Add and specify changes form on the order case page, select **Add**.

    2.  On the Add orders to case window, select one or more orders and select **Add**.

        Order case lines are created corresponding to the order records.

    3.  Select the order case lines you want to edit and select **Edit**.

        Select a single order case line to make specific changes to a specific order. Select multiple order case lines to make the same changes for all orders.

        **Note:**

        If you no longer want to make changes to an order case line item, select it, select the drop-down button next to **Edit**, and select **Delete** to remove it from the list of items to be modified.

    4.  Modify any or all of the values in the Edit item dialog box.

        |Field|Description|
        |-----|-----------|
        |Requested expected date|The date you want your order to be fulfilled.|
        |Requested shipping location|The location to which you want your order to be shipped.|

    5.  Select **Update**.

    6.  Select **Next** on the Add and specify changes form.

5.  Verify the requested changes and submit the order case on the Review and submit page.

    -   If you need to make more changes, navigate to the required page from the Activities section and repeat the modification process.
    -   If the changes are accurate, select **Submit**.

## Result

The order case is created with the order case lines corresponding to the orders you updated, and the state of the order case changes to New.

