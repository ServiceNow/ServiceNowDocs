---
title: Hide supplier pricing from ShoppingHub
description: When creating model categories for grouping your product models, you can decide if pricing is to be displayed in ShoppingHub for supplier products associated to a particular category.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Hide supplier pricing from ShoppingHub

When creating model categories for grouping your product models, you can decide if pricing is to be displayed in ShoppingHub for supplier products associated to a particular category.

The pricing that is displayed for supplier products on ShoppingHub is an agreed-upon contractual price between you and the supplier. As an administrator, based on your business requirement, you can decide if this pricing needs to be displayed or hidden in your ShoppingHub catalog for supplier products associated to a particular category. If you decide to hide the pricing, the shipping and taxes involved are also hidden. If there are parent and child categories, the display pricing choice made on the child category overrides its parent.

If pricing is hidden in the model category form for a product category, pricing details aren’t displayed in the following instances:

-   Product information card on the ShoppingHub catalog
-   Product details or categories or suggestions based on your role landing page
-   Supplier product card, on both ShoppingHub and Virtual Agent
-   Product header card in your shopping cart
-   Summary section during full checkout and also on Virtual Agent
-   Quick checkout overlay
-   Purchase confirmation page after quick and full checkouts
-   **Total line amount** and **Budget** fields in the My purchases list view, on both desktop and mobile
-   **Total line amount** in the header, and price fields **Subtotal**, **Tax**, **Shipping**, and **Total line amount** in the purchase section in the Purchase details page, on both desktop and mobile
-   Activity stream in My purchases
-   **Pre-payment amount** field in the **Pre-payments** tab on the purchase details page
-   **Negotiated unit cost** field in the **Additional quotes** tab on the purchase details page
-   **Total line amount** field in the **Submitted purchases** tab on the purchase details page
-   Approval to-do in the **To-dos** tab on the purchase details page
-   **Total line amount** and **Remaining amount** fields in the blanket purchase list view, on mobile
-   **Total line amount** and **Remaining amount** in the blanket purchase form view header, on mobile
-   **Total line amount** field in the Submitted purchases related list of a blanket purchase order, on mobile
-   **Negotiated unit cost** and **Total line amount** fields in the Additional quotes related list of a blanket purchase order, on mobile
-   Confirmation page after completing a select a supplier to-do
-   Line amount invoiced in invoice acknowledgment

    **Note:** This applies only if you haven't installed the Shopping Hub plugin and are still using the Source-to-Pay Common Architecture plugin.

-   Invoice amount to review in invoice acknowledgment, on mobile
-   Price fields **Total amount**, **Amount paid**, and **Remaining balance** in the purchase section in invoice acknowledgment, on mobile
-   Price fields **Total estimated tax**, **Total estimated shipping**, and **Total amount** in the purchase section in receipt acknowledgment, on mobile
-   Price fields **Subtotal**, **Estimated tax**, **Estimated shipping**, and **Total line amount** in the purchase section in milestones, on mobile
-   **Payout amount** field in the to-do section in milestones, on mobile
-   Activity stream and purchase summary in My to-dos
-   Standard search results on Employee Center \(EC\) and Virtual Agent
-   AI Search results on ShoppingHub, Service Portal, and EC

    **Note:** Even if supplier pricing is hidden, sort by price and filter by price range display search results in ShoppingHub. For sort by price low to high, for example, request pricing products are displayed first, followed by pricing hidden products, and products with price. For filter by price range, if the minimum price range is greater than zero, pricing hidden products are hidden along with request pricing products.


However, when an approval to-do is created, the pricing is visible to the approver so that an informed decision can be taken on the approval request. If display pricing is set to No, then the select a supplier to-do is assigned to the buyer instead of the person who submitted it. But, if the buyer reassigns it to the submitter, the latter can view the price in the to-do in ShoppingHub. This is applicable to both desktop and mobile versions.

Also, if you’re a shopper with store credits allocated to you, you can view the pricing details even though the pricing is otherwise hidden.

**Note:** This hide pricing feature doesn’t impact the checkout flows, sourcing flows, or any other flows that are run in the back-end.

**Parent Topic:**[Using Shopping Hub](use-shoppinghub-portal.md)

