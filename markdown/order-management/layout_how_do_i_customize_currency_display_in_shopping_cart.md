---
title: Customizing the currency display in the shopping cart
description: Configure how currency values appear in the CPQ shopping cart. You can choose to display amounts with the ISO code \(USD 25.99\), currency symbol, or plain numbers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/layout\_how\_do\_i\_customize\_currency\_display\_in\_shopping\_cart.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up pricing display, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Customizing the currency display in the shopping cart

Configure how currency values appear in the CPQ shopping cart. You can choose to display amounts with the ISO code \(USD 25.99\), currency symbol, or plain numbers.

Administrators can customize how currencies are displayed in the CPQ shopping cart.

The CPQ shopping cart displays amounts according to the Currency ISO Code partner field passed from the Salesforce.com \(SFDC\) quote. Unless SFDC is customized in this area, the quoteʼs currency will determine the ISO currency code for CPQ. If no ISO currency code is provided, CPQ defaults to USD.

## Shopping cart currency display options

By default, the shopping cart displays the ISO code to the left of the currency amount.

\[Omitted image "cpq-layout-currency-display-iso-code.png"\] Alt text: shopping cart currency display options

However, the currency symbol can be displayed instead.

\[Omitted image "cpq-layout-currency-display-symbol.png"\] Alt text: shopping cart currency display options

## Setting the shopping cart currency display with the layout editor

The shopping cart currency display is defined in the layout properties, which can be found in the layout editor. For more information, see [Customizing the CPQ UI header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/layout_how_do_i_customize_the_logik_io_ui_header.md)

\[Omitted image "cpq-layout-currency-display-settings.png"\] Alt text: shopping cart currency display options

Three currency display options are available:

-   USD 25.99: Displays currencies with their currency code
-   $25.99: Displays currencies with their currency symbol
-   25.99: Displays currencies as numbers

**Related topics**  


[Show rollup pricing in the shopping cart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[How price is displayed on a layout with multiple BOMs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/how_does_pricing_on_multiple_boms_displayed_on_a_layout_behave.md)

