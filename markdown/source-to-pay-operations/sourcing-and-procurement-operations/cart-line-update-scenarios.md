---
title: Cart line update scenarios
description: Cart lines are created, updated, or deleted based on the updates that you make to the products in your shopping cart.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Shopping cart, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Cart line update scenarios

Cart lines are created, updated, or deleted based on the updates that you make to the products in your shopping cart.

-   A new cart line is created for every new product that you add to your shopping cart.
-   If an existing cart line is created through one method, and you go back to the same product details page and add more through another method, first by quantity and then by budget for example, the existing cart line is updated accordingly without creating a new cart line. In this scenario, when you add by budget, quantity is back-calculated. Similarly, when you add by quantity, the corresponding budget is calculated by multiplying the quantity with the contractual price.

    **Note:** Cart line updates by budget are not supported for bundled products.

-   If you set a new delivery location in the secondary navigation bar or switch users while shopping, and add the same supplier product to your shopping cart, a new cart line is created.
-   If the individual cart lines contain different currencies, the values are displayed in the reference currency in the Summary section. If a single currency exists for all the cart lines, the same is displayed in the Summary section. The price in the cart line continues to be in the contractual price currency.
-   When you remove a product from your cart, the cart line is updated to reflect the status of the product, which is now Pending Deletion. If you wish to add the removed product back to your cart, and select **Undo**, the cart line status is updated to Visible in Cart.
-   If you wish to buy a product at a later date or time, and select **Purchase later**, the cart line status is updated to Purchasing Later.

    ![Product moved to the Purchase later section to your shopping cart when you decide to buy it at a later time](../image/spo-purchase-later.png)

-   If you move a product, some quantity of which already exists in your cart, from your **Purchase later** section to your shopping cart, the cart lines merge and the purchase quantity is updated accordingly.

**Parent Topic:**[Shopping cart](../concept/shopping-cart.md)

