---
title: Multi-currency support in Shopping Hub
description: Shoppers can view and select their local currency during shopping in Shopping Hub, providing a seamless multi-currency experience.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [My purchases on Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Multi-currency support in Shopping Hub

Shoppers can view and select their local currency during shopping in Shopping Hub, providing a seamless multi-currency experience.

## Key benefits

The multi-currency functionality provides the following benefits:

-   Enables shoppers to view prices in their familiar local currency, helping them make more informed purchasing decisions.
-   Enables shoppers operating across multiple geographies to toggle between currencies, providing better context for purchase decisions.
-   Enables approvers to view product prices in their local currency alongside the original supplier currency across email notifications and To-dos.

## How to configure

Role required: sn\_shop.procurement\_administrator

Plugin required: Shopping Hub \(sn\_spend\_uib\)

Ensure that you complete the following configurations for the multi-currency functionality to work correctly in Shopping Hub.

-   Set the `sn_spend_uib.local_currency.enable.menuoption` system property to enable shoppers to view product prices in local currency in Shopping Hub. For more information, see [Components installed with Sourcing and Procurement Operations](../reference/installed-with-FSC.md).

    **Note:** Property is set to True by default. If you do not want prices to be displayed in the local currency, set this property to False.

-   Ensure that each sys\_user record is associated with an organization.

    ![Organization field for a user.](../image/sh-user-org.png)

    This allows the organization’s local currency to become the user’s default currency upon login.

    ![Local currency for the organization.](../image/sh-local-currency.png)

    **Note:** This is the Legal Entity record. On this record, you can view the local currency associated with the legal entity.

-   To display a currency in the **View prices in** drop-down list on the Shopping Hub home page, a corresponding Currency record must exist in the fx\_rate table and be active.

    ![Exchange rate table.](../image/exchange-rate-table.png)


## How it works

The following points describe how the multi-currency feature works:

-   Shoppers can select the currency they want to view during shopping.![View local currency](../image/sh-view-currency.png)

    When a shopper selects a currency, the following banner message appears.

    ![Currency banner.](../image/sh-currency-banner.png)

-   For delegated shopping, the default currency is derived from the delegator’s legal entity.
-   Estimated prices are displayed consistently across supplier cards, product details, cart, checkout, and purchase tracking pages.

    ![Estimated prices for a product in Shopping Hub.](../image/sh-estimated-prices.png)

-   As an approver, you can view the product price in your local currency alongside the original supplier currency. This information appears in email notifications and To-dos in Employee Center and Shopping Hub.
-   The product price is also displayed in both your local currency and the original supplier currency on the product bundle page.

**Parent Topic:**[My purchases on Shopping Hub](my-purchases.md)

