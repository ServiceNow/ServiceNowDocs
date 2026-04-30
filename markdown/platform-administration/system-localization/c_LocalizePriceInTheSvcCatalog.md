---
title: Localizing currency and price fields
description: You can localize currencies for item prices and options.
locale: en-US
release: zurich
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring System Localization, System Localization, Translation and localization, Configure core features, Administer]
---

# Localizing currency and price fields

You can localize currencies for item prices and options.

Standard currency fields display the same price in different currencies based on the user's language. A price field is similar to a currency field, but with special features for conversion and display.

The system has the concept of a reference currency based on the instance locale. All currency values are automatically converted to the reference currency before aggregation or conversion. Do not change the global locale setting after you have data in the system. Changing the global locale setting after adding data to the system can cause aggregations to calculate and display incorrectly. For information about configuring the instance locale, see [Configuring locales](c_DefineLocales.md#).

**Related topics**  


[Currency administration](../../currency/concept/currency.md)

[Price fields](../../currency/concept/price-fields.md)

[Default currency values in scripts](../../currency/concept/currency-values-scripts.md)

