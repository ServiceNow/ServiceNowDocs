---
title: Enable user actions
description: Configure the edit and cancel options to enable modifications to the purchases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-request-revisions.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [ShoppingHub configuration, Set up master data, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Enable user actions

Configure the edit and cancel options to enable modifications to the purchases.

## Before you begin

Role required: sn\_spend\_psd.psd\_admin, sn\_shop.procurement\_administrator

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Administration** &gt; **ShoppingHub Configuration**.

2.  Select purchase modification type, for example, **Cancel purchase order** to modify the details.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the configuration|
    |Configuration type|Select the type from the available list. For example, user interface|
    |Active|Check box to determine the active status of this configuration|
    |Page|Page information for Shopping Hub configuration|
    |Section|Section information for Shopping Hub configuration, for example, User actions|
    |Object|Details of the object name, for example, Purchase order|
    |Purchase modification type|Details of the modification, for example, Cancel|
    |Content type|Details of the content type, for example, Label|
    |Display label|Name of the configuration label, for example, cancel purchase order|
    |Buttons|Details of the available options|
    |Record producer|Select the record producer. For example, **Cancel purchase order**|

4.  Select **Update** or select **Save** from the additional actions menu.


## What to do next

Use the same steps to modify the following user action configurations:

-   Edit purchase order
-   Cancel purchase order line
-   Edit purchase order line
-   Edit purchase request
-   Cancel purchase request
-   Edit purchase request line
-   Cancel purchase request line

You may add additional configurations to suit your business requirements.

**Note:** When a user shops on behalf of another user, the actions on the purchase cards, such as cancel and edit, are shown only if the `sn_spend_uib.purchased_behalf.enable.card_actions` property is set to true, or if the purchase belongs to the user that they are shopping as. If an action is missing for a user who shops on behalf of others, check this property.

**Note:** The actions on the purchase cards are read from the ShoppingHub Configuration records. Only users with the `sn_shop.shopper` or `sn_shop.shopping_hub_admin` role can read these records. A user without one of these roles does not see the configured actions, such as Cancel purchase order.

**Parent Topic:**[ShoppingHub configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/shoppinghub-configurations.md)

