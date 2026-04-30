---
title: Single-currency mode
description: Single-currency mode enables all users of the platform to view currency values in the same currency.
locale: en-US
release: xanadu
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Standard currency fields, Exploring currency administration, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Single-currency mode

Single-currency mode enables all users of the platform to view currency values in the same currency.

Before enabling single-currency mode, set the system locale. To configure single-currency mode, set the following properties:

-   **glide.i18n.single\_currency**: **true** or **false**
-   **glide.i18n.single\_currency.code**: the three-letter ISO currency code
-   **glide.system.locale**: the system locale

**Note:** For detailed information about valid locale formats, see [Locale settings](locales.md).

Using the single-currency mode has the following limitations:

-   The single-currency mode changes the currency that appears in the user views, but does not change the number formatting. Even though users in different countries see currency values in one currency, the number formatting, as determined by the user’s locale, might not be what they expect.
-   Price fields, which have flexible conversion and currency features, can't be used because currency value input is constrained to the single currency.

You can avoid the effects of rate conversions by setting the system locale and the reference currency to be the single currency.

**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

