---
title: Purchase an L1 punchout item on behalf of another user
description: Purchase items from a Level 1 \(L1\) punchout supplier site on behalf of another user. Select a business owner before the redirect so that items are placed in the correct user's cart.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/purchase-l1-punchout-on-behalf.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-05"
reading_time_minutes: 2
breadcrumb: [Purchase punchout items for another user, Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase an L1 punchout item on behalf of another user

Purchase items from a Level 1 \(L1\) punchout supplier site on behalf of another user. Select a business owner before the redirect so that items are placed in the correct user's cart.

## Before you begin

Verify that the administrator has configured the "Buy on Behalf of" shopping control so that you have at least one eligible business owner to select. The target business owner must be a member of the punchout group required for the supplier you want to purchase from. For more information, see [Purchase punchout items on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-punchout-on-behalf-sh.md).

**Note:** The requirement for the target business owner to be a member of the supplier's punchout group applies only to L1 punchout suppliers.

Role required: sn\_shop.shopper

## About this task

You can purchase an L1 punchout item on behalf of another user from a punchout search result, a supplier or product card, or the Browse supplier page. Entry points are also available on the Home page, Supplier landing page, Product category page, and in Employee Center.

Plugin required: Shopping Hub \(sn\_spend\_uib\)

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **ShoppingHub Home**.

2.  Search for or browse to a punchout product or service, and select the item.

    The **Which user are you shopping for?** dialog box opens.

3.  Select one of the following options:

    -   To shop using your own credentials, select **Myself**.
    -   To shop on behalf of another user, select **On behalf of another user**, and then select the business owner from the **On behalf of** list.
    \[Omitted image "sh-on-behalf-modal.png"\] Alt text: Dialog box with On behalf of another user selected and Alan Edwards chosen in the On behalf of list.

4.  Select **Confirm**.

    If the selected business owner is eligible for the punchout supplier, you are redirected to the punchout supplier site using that user's credentials and punchout group membership.

    If the selected business owner isn't eligible, a validation message is displayed and you aren't redirected.

    \[Omitted image "sh-on-behalf-error.png"\] Alt text: Dialog box showing Warren Summers selected with a validation error: Selected user is not eligible for punchout with this supplier.

5.  On the punchout supplier site, add the required items to your cart, and then return to Shopping Hub or Employee Center to complete checkout.

    \[Omitted image "sh-on-behalf-cart.png"\] Alt text: Alan Edwards's shopping cart showing two items from 3CLogic, Inc. with an estimated total and Proceed to checkout button.

    For more information, see [How L1 punchout works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/level-one-punchout.md)


## Result

The items you added on the punchout supplier site are placed in the cart of the selected business owner. If you didn't select a business owner, the items are placed in your own cart.

**Parent Topic:**[Purchase punchout items on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-punchout-on-behalf-sh.md)

