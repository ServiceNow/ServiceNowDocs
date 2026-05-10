---
title: Add a catalog item to the shopping cart
description: Add a catalog item or order guide to the shopping cart to store at one place and checkout.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Catalog in Service Portal, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a catalog item to the shopping cart

Add a catalog item or order guide to the shopping cart to store at one place and checkout.

## Before you begin

Role required: requester

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home**.

    The Service Portal homepage is displayed.

2.  Select a catalog item or order guide from Service Catalog.

3.  Click the Add to Cart icon \(![Icon to add to cart](../image/IconAddTocart.png)\) in the Ordering widget.

    **Note:**

    -   You can add the same item to the cart multiple times. Every time you add an item to the cart, a new instance of the item is created.
    -   The cart information is automatically updated in all open tabs or windows.
4.  Click **View Cart** from the confirmation message or the **Cart** menu option on the main navigation bar.

    The cart details page is displayed.

5.  To navigate to any cart item page, click the image or name of an item in the cart details page.

    **Note:** This step does not open a new instance of the item, but the instance that is in the cart, where you can edit the details.

6.  If required, edit the quantity of items.

7.  To remove an item from the cart, click the Remove Item icon \(![Icon to remove item](../image/RemoveIcn.png)\).

8.  To navigate to the Service Catalog landing page, click **Continue Shopping**.

9.  To clear the cart, click **Clear Cart**.

10. To create a bundle from the cart:

    1.  Click **Save as Bundle**.

    2.  In the Create New Bundle window, specify the **Bundle Name** and select the items that you want to include.

    3.  Click **Save**.

    **Note:** When you create a bundle from the cart, which includes an order guide, the association of the items to the order guide is lost.

11. To add a saved bundle to the cart, open the bundle from the **My Saved Bundles** section and click **Add to Cart**.

12. To replace the cart items with a saved bundle, open the bundle from the **My Saved Bundles** section and click **Replace Cart**.

13. Click **Proceed to Checkout**.

    The Order Confirmation window is displayed.

14. From the **Request for** list, select the user for whom you are requesting.

    **Note:**

    -   By default, the user who is logged in is selected in this list.
    -   The User \[sys\_user\] table columns specified in the **Additional columns for the “request for” Service Catalog widget. Choose fields in the sys\_user table. Must be semicolon separated** \(**glide.sc.request\_for.columns**\) Service Catalog property are displayed in the **Request for** list and you can search for a user by the specified columns.
    -   You can provide additional widget options to control the **Request for** default value. For example:

        ```
        "requested_for_id": { 
        "value": "62826bf03710200044e0bfc8bcbe5df1" 
        }, 
        "requested_for_display": { 
        "value": "Abel Tuter" 
        }
        ```

15. If required, specify the **Delivery Information** and **Special instructions**.

16. To add one or more attachments for the cart, click the add attachments icon \(![add attachment icon](../image/IconAddAttachmnt.png)\).

    You can browse and choose the files, drag the files, or copy and paste them in the Add attachments window.

17. Click **Checkout**.

    The corresponding request is displayed in the Order Status page with the request number, estimated delivery date for the entire order, price, and the order status of individual ordered items.

    **Note:**

    -   Use the instance options on the Order Status page to display the pre-defined columns.
    -   You can display either the RITM number or the name of the catalog item. By default, the name of the catalog item is displayed.

**Parent Topic:**[Service Catalog in Service Portal](../concept/catalog-on-portal.md)

**Related topics**  


[Access Service Catalog categories in Service Portal](access-categories-portal.md)

[Add an item to the wish list in Service Portal](add-to-wishlist-portal.md)

[Request a catalog item from Service Portal](request-cat-item-portal.md)

[Request an order guide from Service Portal](request-order-guide-portal.md)

[SC Shopping Cart widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/sc-shopping-cart.md)

