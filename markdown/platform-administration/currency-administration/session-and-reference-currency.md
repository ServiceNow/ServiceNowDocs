---
title: Session and reference currency
description: The default, or standard, currency fields in the ServiceNow AI Platform use two kinds of currency, Session and Reference.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Standard currency fields, Explore, Currency administration, Configure core features, Administer]
---

# Session and reference currency

The default, or standard, currency fields in the ServiceNow AI Platform® use two kinds of currency, Session and Reference.

-   **Session currency**

    The session currency is defined for the user by the user’s locale or single-currency mode.

-   **Reference**

    The system local determines the reference currency, and is the standard used across the entire instance.


Each time you enter a value into a currency or price field, the system stores three pieces of information:

-   Value as entered, in the user's locale.
-   Currency code, in the user's locale.
-   Value converted to the reference currency using the current exchange rate.

**Note:** In multiple-currency mode, the currency code saved in the currency field may not be the same as the session currency code. For example, the session currency could be the Euro and the number entered could be the Japanese Yen.

## Session currency

When users view a currency value, they can see the value as entered or in the session-currency format. The format contains the:

-   Currency symbol
-   Value converted to the session currency and shown in a localized number format.

The user’s locale determines the session currency format.

The number format can differ in features such as the decimal separator based on the locale. For example, the US formatting is 1,234,567.89, while German formatting is 1.234.567,89. The ServiceNow AI Platform® determines the session currency in the following sequence:

-   Single-currency mode setup using **glide.i18n.single\_currency** and**glide.i18n.single\_currency.code**.
-   Default currency for the user’s locale.

## Reference currency

To perform calculations on heterogeneous currency values, the ServiceNow AI Platform® stores currency values converted to a system currency, referred to as the reference currency. Every currency field contains a reference currency value. The system determines the reference currency in the following sequence:

-   System locale set using the property **glide.system.locale**
-   Java default locale, typically en.US

The filtering and aggregation features use the reference currency value to perform calculations on default currency fields. These features can yield inaccurate results because of conversion rate changes.

## Issues with currency fields

Users are often confused by the results of filtering, sorting, and displaying currency fields because the system works with at least two currencies for each value: the session currency and the reference currency.

**Note:** Aggregations and filtering of currency fields use the reference currency, and the user sees the session currency. Because of changing conversion rates, the filtered reference currency values might not result in the same order as the session currency values would suggest. The same issue happens with aggregations.

The user might see the following issues:

-   Lists filtered on currency fields might not be in the expected order. It uses the reference currency values for filtering but displays session currency values.
-   Aggregation of currency fields may not produce the expected results because reference currency values are aggregated, and then converted to the session currency.
-   Currency values may not appear as expected because currency values are formatted based on the user's locale and not on the currency code.

This confusion may be the result of the difference between session and reference currencies, changing conversion rates, and different session currencies used by different users.

**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

