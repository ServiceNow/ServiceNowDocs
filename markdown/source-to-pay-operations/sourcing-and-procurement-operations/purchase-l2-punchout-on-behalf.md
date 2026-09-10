---
title: Purchase an L2 punchout item on behalf of another user
description: Select a business owner when you request to buy or add a Level 2 \(L2\) punchout item to your cart. This validates eligibility and attributes the resulting order to the correct user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/purchase-l2-punchout-on-behalf.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-05"
reading_time_minutes: 2
breadcrumb: [Purchase punchout items for another user, Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase an L2 punchout item on behalf of another user

Select a business owner when you request to buy or add a Level 2 \(L2\) punchout item to your cart. This validates eligibility and attributes the resulting order to the correct user.

## Before you begin

Verify that the administrator has configured the "Buy on Behalf of" shopping control so that you have at least one eligible business owner to select. For more information, see [Purchase punchout items on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-punchout-on-behalf-sh.md).

Role required: sn\_shop.shopper

## About this task

Unlike L1 punchout, an L2 punchout item is searched, viewed, and added to your cart within Shopping Hub without redirecting to the punchout supplier site. You choose whether you're purchasing for yourself or on behalf of another user when you request to buy or add the item to your cart.

Plugin required: Shopping Hub \(sn\_spend\_uib\)

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **ShoppingHub Home**.

2.  Search for or browse to a punchout product or service, and select the item.

3.  Choose whether you're purchasing for yourself or on behalf of another user.

    -   To purchase using your own credentials, choose **Myself**.
    -   To purchase on behalf of another user, choose **On behalf of another user**, and then select the business owner from the **On behalf of** list.
    \[Omitted image "sh-l2-on-behalf-modal.png"\] Alt text: Product purchase page with Purchase on behalf of check box selected and name field populated.

    If the selected business owner is a member of the punchout group required for the item, the item is added to your cart, or your request to buy proceeds, on that user's behalf. If the selected business owner isn't eligible, the item isn't added and a validation message is displayed.

4.  Select **Confirm**.

    If the selected business owner is a member of the punchout group required for the item, the item is added to your cart, or your request to buy proceeds, on that user's behalf.

    If the selected business owner isn't eligible, a validation message is displayed and you aren't redirected.

    \[Omitted image "sh-on-behalf-error.png"\] Alt text: Dialog box showing an ineligible user selected with a validation error: Selected user is not eligible for punchout with this supplier.

5.  Complete the checkout in Shopping Hub.

    Checkout creates a purchase requisition, and upon approval, a purchase order that's synced with the punchout system. For more information, see [How L2 punchout works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/level-two-punchout.md).


## Result

The order created from this purchase is attributed to the selected business owner. If you didn't select a business owner, the order is attributed to you.

**Parent Topic:**[Purchase punchout items on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-punchout-on-behalf-sh.md)

