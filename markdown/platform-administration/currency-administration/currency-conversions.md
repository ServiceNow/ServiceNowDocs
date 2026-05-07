---
title: Default currency conversions
description: Currency values can be converted to other currencies when stored and accessed.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Defaults required for standard currency use, Configure, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Default currency conversions

Currency values can be converted to other currencies when stored and accessed.

Conversions can happen in these situations.

-   The currency value converts to the reference currency when stored, whether on insert or update. The reference currency value is saved as well as the currency value.
-   The currency value converts to the user’s session currency for display.
-   The value entered into a filter converts to the reference currency using the currency specified in the filter.

Conversion rates are stored in the Exchange Rate \[fx\_rate\] table. Each record contains the conversion rate from a given currency to the Euro. The rates are updated daily from the ECB website by a scheduled job called Update Currency Conversion Rates.

A currency conversion from one currency to another involves two rates.

-   Actual: In the Exchange Rate table, each record contains the conversion rate from a given currency to the Euro.
-   Expected: In the Exchange Rate table, each record contains the conversion rate from the Euro to the given currency.

Whenever you perform a conversion, it uses the latest conversion rates. Therefore, calculations can potentially yield unexpected results. For example:

-   Different currency values can have different rates applied to them while storing the reference currency value. Therefore, aggregation can combine values at different rates and convert back at another rate.
-   A filter value is converted at current rates while the values it filters in the database can be converted at different rates. A filter for $100 at today's rate can match a value of $99 obtained at yesterday’s rates.

**Note:** For display purposes, the currency value used is what the user entered converted to session currency. However, for aggregation and filtering, the reference currency value is used. Using the reference currency enables currency values converted at different rates to be compared together.

-   **[Schedule the rate update job](../../localization/task/t_SetAConversionRate.md)**  
Schedule the Update Currency Conversion Rates job to perform a nightly download of currency-conversion tables from the European Central Bank.
-   **[Use your own currency-conversion rates](../../localization/task/t_UseYourOwnConversionTable.md)**  
All currency conversions are based on the rates stored in the Exchange Rate table. You can turn off the regularly scheduled update from the European Central Bank \(ECB\), and maintain the table manually.

**Parent Topic:**[Setting up defaults required for standard currency use](setting-up-standard-currency-defaults.md)

