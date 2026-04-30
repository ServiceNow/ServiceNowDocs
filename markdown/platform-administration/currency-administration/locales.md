---
title: Locale settings
description: There are two locale settings, system and user. The system locale determines the reference currency, and the user locale determines the session currency.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Standard currency fields, Exploring currency administration, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Locale settings

There are two locale settings, system and user. The system locale determines the reference currency, and the user locale determines the session currency.

## System locale

You set the system locale using the **glide.system.locale** property. The value is in the format `Language.Country`, where the:

-   `Language` is an ISO 639 language code.
-   `Country` is an ISO 3166 language code.

Internally, this value is used as specified by Java. The system locale setting should be in the [Java supported locales](http://www.oracle.com/technetwork/java/javase/javase7locales-334809.html) list. Set the system locale once after a fresh zBoot, because reference currency values that appear in currency fields are in the currency implied by the system locale. To set this property, see [Control default currency field configuration and use in an instance](../reference/currency-properties.md).

**Note:** Do not change the system locale after currency values have been entered into the instance. When you change the system locale, the reference currency values are not adjusted. There is no rate conversion. This persistence results in invalid aggregations and filtering.

## User locale

The ServiceNow AI Platform® determines the user locale in the following sequence:

-   User record in which the country, or both the country and language, are specified.
-   System locale set using the **glide.system.locale** property.
-   Browser locale.

Amounts in currency fields are composed of a currency code and amount. Amounts always appear in the session currency, and are formatted in the Java-specified format for the user locale.

**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

