---
title: Order a product with quick checkout
description: Order a product or service that you want to purchase from the product catalog available on Shopping Hub Home.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Order a product with quick checkout

Order a product or service that you want to purchase from the product catalog available on Shopping Hub Home.

## Before you begin

Role required: sn\_shop.shopper

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **ShoppingHub Home**.

    If you’re shopping for someone else as a delegate, select the appropriate shopper from the **Shopping as** list.

    **Note:** This option is visible only if you’re [configured to delegate for another employee shopper](configure-delegate-for-a-shopper.md).

2.  Browse for the required product or service using the **Categories** or the **Suppliers** list on the Shopping Hub homepage, or search for it.

    If you’re a returning shopper, you can also find your recently viewed items on the homepage.

    On the product details page, you can see the price of the product and the probable date of its delivery.

    If pricing isn’t available and the supplier must be contacted for it, you can see the probable date by which you can get the pricing details. For more information, see [Complete sourcing checkout](complete-sourcing-checkout.md).

3.  To place an order for a product or service that has pricing:

    1.  Select **Quantity** or **Budget** as appropriate.
    2.  Enter the quantity that you need or the budget at your disposal.

        **Note:** The budget you provide automatically calculates the quantity for the product and the corresponding price. While entering the price, you can change your currency type from the list.

    3.  Do one of the following actions:
        -   Select **Request to buy** to perform a quick checkout with your selected product.
        -   Select **Add to cart** to save your product to your cart and continue shopping.

            **Note:** For more information on how to use your shopping cart, see [Shopping cart](../concept/shopping-cart.md).

            ![Order a product with quick checkout](../../source-to-pay-operations/image/spo-order-quick-checkout.png "Order a product with quick checkout")

    4.  On the quick checkout form, fill in the fields.

<table id="table_gz1_scj_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Where do you want this delivered?

</td><td>

Location where you want your product to be delivered. The options are:-   To a saved location

**Note:** The recipient is the logged-in user or the delegated user.

-   To a work address \(already approved\)
-   To somewhere else


</td></tr><tr><td>

When do you need this product?

</td><td>

Date range when you want your product to be delivered. The options are:-   As soon as possible: For the quickest delivery slot possible for the product. This is calculated based on the product category of the selected product.
-   A specific date
-   I have a time frame in mind \(a blanket order\)
**Note:** You can select a date or date range that is in the past, present, or future. If you select a date range, you must enter your requested start and end dates to proceed.

</td></tr><tr><td>

Payment method

</td><td>

Method of making the payment. Select a cost center from the list, which is defaulted with your assigned cost center. You can also add multiple cost centers, if necessary, and save them for future use.**Note:** Verify that the total percentage of all the cost centers doesn’t exceed 100%.

You can view the cost center and allocation breakup from the purchase requisition that is created, by navigating to the Cost Allocations related list of the associated purchase requisition line.

If you have available credits, the same is displayed here as a mode of payment. For details, see [Shop with employee credits](shop-employee-credits.md).

</td></tr></tbody>
</table>        **Note:** If you change the quantity or delivery location during checkout, the shipping and tax estimates are recalculated and updated accordingly. The cart line is also updated with the new estimates.

    5.  Based on whether the purchase is for an existing project, select one of these options.

<table id="table_rcj_lvm_1xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

No

</td><td>

Purchase isn’t for an existing project.

</td></tr><tr><td>

Yes

</td><td>

Purchase is for an existing project. Enter the project details as required.**Note:** You must have the Procurement with Project Management \(sn\_spend\_ppm\) application installed, and also have the IT Project User role. For more information, see [Sourcing and Procurement Operations integration with Project Management](../concept/integration-psm-ppm.md).

</td></tr></tbody>
</table>    6.  In the **Purchase reason** field, provide your reason for making the purchase.

        ![Purchase reason and watchlist for the purchase request](../../source-to-pay-operations/image/spo-pr-watchlist.png "Purchase reason and watchlist for the purchase request")

    7.  In the **Watchlist** field, select one or more users to be added to the watchlist of the purchase request.

        The users on the Watchlist receive email notifications when specific conditions are fulfilled and the purchase request status is updated. By default, you can add up to 20 users in the watchlist. You can modify this value by configuring the system properties. For more information, see [Components installed with Sourcing and Procurement Operations](../reference/installed-with-FSC.md).

        **Note:** This limit for the number of users on the watchlist is applicable only while making the purchase request. You can add more users to the watchlist after the purchase request is created. However, you can add more users only at the purchase requisitions page.

    8.  Add any supporting documents for this purchase as attachments, if applicable.

        **Note:** You can download, remove, or rename the attachments, as required. These attachments are also appended to the associated purchase requisition for reference.

    9.  Select **Submit request**.

## What to do next

-   Review your purchase. After you complete your checkout, select **Review your purchase** to view the details or your order.
-   To review your orders anytime later, you can select **My purchases** from your profile on ShoppingHub.

    -   View the list of all purchases placed from your shopping account.
    -   Track the progress of an order, review to-dos, and so on.
    **Note:** For more information, see [My purchases](../concept/my-purchases.md).


**Parent Topic:**[Using Shopping Hub](../reference/use-shoppinghub-portal.md)

