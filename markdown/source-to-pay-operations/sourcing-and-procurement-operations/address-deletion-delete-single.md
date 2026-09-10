---
title: Delete a saved address
description: Shoppers can delete saved delivery addresses they no longer need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/address-deletion-delete-single.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [delete address, remove address, shopping preferences]
breadcrumb: [Using Shopping Hub, Use Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Delete a saved address

Shoppers can delete saved delivery addresses they no longer need.

## Before you begin

Role required: sn\_shop.shopper

## About this task

When a non-default address is deleted, it is immediately removed from the saved addresses list and a success confirmation appears. If the deleted address is the current default delivery location, you must select a new default before the deletion completes. For more information about address deletion permissions, see [Address deletion permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/address-deletion-access-control.md).

When you delete an address, the following happens:

-   Single address removal: When you delete a work address you no longer use, a success notification confirms the deletion.
-   Bulk deletion: You can remove multiple addresses at once using the Manage saved addresses modal. You cannot delete all addresses at once and must keep at least one saved address.
-   Deleted addresses do not appear: Deleted addresses are hidden from the delivery location picker at checkout.
-   Work address directory is unaffected: When adding a new work address from the org directory, previously deleted addresses are visible and can be re-added to the saved list.
-   Re-addition restores functionality: You can re-add a previously deleted address from the work address picker to restore it to your saved list.

## Procedure

1.  From the Shopping Hub home page, select the **Deliver to** drop-down list.

2.  Select the **Manage addresses** link.

    \[Omitted image "spo-manage-addresses.png"\] Alt text: Deliver to drop-down showing saved delivery addresses and the Manage addresses link.

    The Manage saved addresses modal opens, displaying all your saved delivery locations.

3.  In the modal, select the box beside the address you want to delete.

    \[Omitted image "spo-remove-address.png"\] Alt text: Manage saved addresses modal with the default address check box selected and the Remove button active.

4.  Select **Remove** to confirm the deletion.

    -   If the address is not the default: The address is immediately removed from the list. A success toast notification confirms the deletion.
    -   If the address is the default: A secondary modal appears asking you to select a new default delivery location before proceeding.
5.  If prompted, select a replacement default address and then select **Remove** again.

    \[Omitted image "spo-remove-default-address.png"\] Alt text: Remove address modal prompting selection of a replacement default address, with Cancel and Remove buttons.

    The old default address is deleted, and the newly selected address becomes your default delivery location.

    \[Omitted image "spo-default-address.png"\] Alt text: Deliver to drop-down showing the newly selected address highlighted as the default delivery location.


## Result

The deleted address is removed from your saved addresses list. The address record is marked as deleted in the system but is not permanently removed, enabling audit and potential restoration if needed.

If you attempt to re-add the deleted address from the work address picker, it will reappear in your saved list with a fresh record.

-   If the deletion fails, the modal closes and an error toast notification appears. The address remains in your saved list. Try again or contact your administrator for assistance.
-   If the **Remove** button is disabled, you have selected all saved addresses. Deselect one address to retain it as your default delivery location, then try again.
-   If the **Manage addresses** link is not visible, you have only one saved address. You must always have at least one default delivery location and cannot delete it.

**Parent Topic:**[Using Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/use-shoppinghub-portal.md)

