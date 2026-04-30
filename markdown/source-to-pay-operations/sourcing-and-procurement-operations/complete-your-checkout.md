---
title: Complete your checkout
description: Proceed to checkout when you’ve completed your shopping and have reviewed your shopping cart.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Complete your checkout

Proceed to checkout when you’ve completed your shopping and have reviewed your shopping cart.

## Before you begin

Role required: sn\_shop.shopper

## Procedure

1.  [Select a delivery location](select-delivery-location.md).

2.  [Select a delivery date](select-delivery-date.md).

3.  [Select a payment method](select-payment-method.md).

4.  [Provide a reason for your purchase](provide-reason-for-purchase.md).

5.  [Add users to the watchlist of the purchase](add-users-watchlist-purchase.md)

6.  Add relevant attachments, if applicable.

    **Note:** You can add attachments at the entire purchase level and also at the individual product level. The purchase requisitions display the attachments added at both the levels. If approvals are required for this purchase, these attachments are available for all the approvers in both Shopping Hub and Employee Center. The automatic approval emails that are triggered also contain the attachments for reference, as needed.

7.  Provide any additional information, if applicable.

    **Note:**

    -   If you decide to go back and update any of your previously selected parameters, be it delivery location, delivery date, payment method, or purchase reason, a warning message is displayed stating that this update shall undo all your selections up to checkout.
    -   The data you enter during checkout are lost in an incomplete checkout process. For more information, see [Checkout data loss scenarios](../reference/checkout-value-retention-scenarios.md).
8.  Select **Complete checkout**.

    Your purchase is requested, and a confirmation page is displayed with the following information:

    -   Message stating that your requested amount, if approved, shall be processed and sent to the supplier, and that you’ll be notified of the same.
    -   Link to view all your purchases. This takes you to the [My purchases](../concept/my-purchases.md) landing page.
    -   What to expect, listing the next steps.
    **Note:** On completing your checkout, an appropriate number of cart lines are created, which then result in the creation of purchase lines. For more information, see [Purchase line creation scenarios](../reference/purchase-line-creation-scenarios.md).


-   **[Select a delivery location](select-delivery-location.md)**  
You can select either a single delivery location or multiple delivery locations for the various products in your cart.
-   **[Select a delivery date](select-delivery-date.md)**  
You can select a single delivery date or multiple delivery dates for the various products in your cart. If you're unsure of a delivery date, you can provide an estimated time frame which then creates a blanket order.
-   **[Select a payment method](select-payment-method.md)**  
You can pay using one of your preferred payment methods or use another cost center to make the payment. You can even pay using multiple cost centers for the various products in your cart.
-   **[Provide a reason for your purchase](provide-reason-for-purchase.md)**  
You must provide a reason for making your purchase. This is mandatory and allows you to complete your checkout.
-   **[Configure additional questions for checkout](configure-additional-questions-for-checkout.md)**  
As an administrator, you can configure additional questions for full checkout to collect more information from a shopper specific to a purchase. This information is first stored in the Requisition Additional Info staging table against the purchase requisition ID that is created on checkout, and then mapped to the Purchase Requisitions table for back-end consumption.
-   **[Configure purchase requisition line-level questions in ShoppingHub](configure-additional-information-prl.md)**  
As a procurement administrator, you can create configurable, line-level questions for shoppers to provide the information needed to complete the purchase during the checkout process in Shopping Hub. These questions are defined in Catalog Builder and specific to certain products or product categories.
-   **[Checkout data loss scenarios](../reference/checkout-value-retention-scenarios.md)**  
The data you enter during checkout are lost in an incomplete checkout process.
-   **[Purchase line creation scenarios](../reference/purchase-line-creation-scenarios.md)**  
On completing your checkout, an appropriate number of cart lines are created, which then result in the creation of purchase lines.

**Parent Topic:**[Using Shopping Hub](../reference/use-shoppinghub-portal.md)

