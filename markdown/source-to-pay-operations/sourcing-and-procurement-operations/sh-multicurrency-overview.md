---
title: Multi-currency support in Shopping Hub
description: Shoppers can view and select their local currency during shopping in Shopping Hub, providing a seamless multi-currency experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/sh-multicurrency-overview.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-10-24"
reading_time_minutes: 2
breadcrumb: [Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
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

-   Set the `sn_spend_uib.local_currency.enable.menuoption` system property to enable shoppers to view product prices in local currency in Shopping Hub. For more information, see [Components installed with Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/installed-with-FSC.md).

    **Note:** Property is set to True by default. If you do not want prices to be displayed in the local currency, set this property to False.

-   Ensure that each sys\_user record is associated with an organization.

    \[Omitted image "sh-user-org.png"\] Alt text: Organization field for a user.

    This allows the organization’s local currency to become the user’s default currency upon login.

    \[Omitted image "sh-local-currency.png"\] Alt text: Local currency for the organization.

    **Note:** This is the Legal Entity record. On this record, you can view the local currency associated with the legal entity.

-   To display a currency in the **View prices in** drop-down list on the Shopping Hub home page, a corresponding Currency record must exist in the fx\_rate table and be active.

    \[Omitted image "exchange-rate-table.png"\] Alt text: Exchange rate table.


## How it works

The following points describe how the multi-currency feature works:

-   Shoppers can select the currency they want to view during shopping.\[Omitted image "sh-view-currency.png"\] Alt text: View local currency

    When a shopper selects a currency, the following banner message appears.

    \[Omitted image "sh-currency-banner.png"\] Alt text: Currency banner.

-   For delegated shopping, the default currency is derived from the delegator’s legal entity.
-   Estimated prices are displayed consistently across supplier cards, product details, cart, checkout, and purchase tracking pages.

    \[Omitted image "sh-estimated-prices.png"\] Alt text: Estimated prices for a product in Shopping Hub.

-   As an approver, you can view the product price in your local currency alongside the original supplier currency. This information appears in email notifications and To-dos in Employee Center and Shopping Hub.
-   The product price is also displayed in both your local currency and the original supplier currency on the product bundle page.

**Parent Topic:**[Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/shopping-hub-overview.md)

