---
title: Request updates for items in a single order
description: Request changes for the expected order fulfillment date, shipping location, or quantity for specific items in an order by creating an order case from the Business Portal.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Business Portal, Use, Sales and Order Management]
---

# Request updates for items in a single order

Request changes for the expected order fulfillment date, shipping location, or quantity for specific items in an order by creating an order case from the Business Portal.

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

This option should be set to **Specific order lines, single order** to create a case for specific order line items in a single order.

</td></tr><tr><td>

Order number

</td><td>

The order for which you want to create the case.

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

4.  Select specific order items that you want to add to the order case.

    1.  Select **Add** on the Add and specify changes form on the order case page.

    2.  On the Add orders line items to case window, select the order items for which you want to create a case and select **Add**.

        Order case lines are created corresponding to the order items you selected.

    3.  Select the order case lines you want to edit and select **Edit**.

        If you no longer want to make changes to an order case line item, select it, select the drop-down button next to **Edit** and select **Delete** to remove it from the list of items to be modified.

    4.  Modify one or more of the values on the Edit item dialog box.

        |Field|Description|
        |-----|-----------|
        |Requested expected date|The date you want your order to be fulfilled.|
        |Requested shipping location|The location to which you want your order to be shipped.|
        |Requested quantity|The quantity of the item you want to purchase.|

    5.  Select **Update**.

    6.  Select **Next** on the Add and specify changes form.

5.  Verify the requested changes and submit the order case on the Review and submit page.

    -   If you need to make more changes, navigate to the required page from the Activities section and repeat the modification process.
    -   If the changes are accurate, select **Submit**.

## Result

The order case is created with the order case line items corresponding to the order line items you updated, and the state of the order case changes to New.

