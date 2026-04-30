---
title: Understanding how FX Currency field conversions work
description: You can use existing system currency rates or define a custom conversion rate table for use in FX Currency processing.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [FX Currency fields, Exploring currency administration, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Understanding how FX Currency field conversions work

You can use existing system currency rates or define a custom conversion rate table for use in FX Currency processing.

A currency conversion rate represents the conversion factor for exchanging one currency for another. The conversion rate is used when converting a currency value, expressed in one currency, to another currency. Conversions can occur for storage \(for example, conversion to a reference currency\) or for display \(for example, conversion to a session currency\).

## When conversions occur

FX Currency fields expose the values inside the Currency Instance \[fx\_currency2\_instance\] record as dot walkable fields. You can access to all data held in an FX Currency field without any transformations. Conversions can happen in these situations:

1.  Calculation of a reference value, calculated when you enter a currency value, whether on insert or update. The reference currency value is saved as well as the currency value as entered. Once this calculation takes place, the reference value is not recalculated.
2.  Calculation of the session display value returned from getDisplayValue\(\), which performs conversions to the required currency.

    The conversion rate is based on the settings of the **Conversion Rate Table** and **Conversion Date Source** fields in **System Localization** &gt; **FX Currency Configuration.**

    **Note:** To learn more about these settings, see [Specify the rate table and date source for currency conversions](../task/fx-currency-conv-rate-table-date-source.md).


## Conversion rates

FX Currency conversion rates are stored in the following ways:

-   System rate \[fx\_system\_rate\] table: Contains system conversion rates. Each record contains the conversion rate from the Euro to a given currency. The rates are downloaded daily from the ECB website by a scheduled job called Retrieve System Rates. To learn more, see [Schedule the rate update job](../../localization/task/t_SetAConversionRate.md).
-   Custom rate table: Contains custom currency conversion rates, and custom rate tables extend the Currency Conversion Rate \[fx\_conversion\_rate\] table. To learn more about creating custom rate tables, see [Add conversion rates using a custom rate table](../task/custom-rate-table.md).

**Parent Topic:**[FX Currency fields](fx-currency.md)

