---
title: FX Currency fields
description: Use FX \(Foreign Exchange\) Currency fields as an alternative to the standard \(default\) currency fields found in most applications. They are highly configurable, support use of custom rate tables, report aggregations, and provide for improved visibility into conversion calculations.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# FX Currency fields

Use FX \(Foreign Exchange\) Currency fields as an alternative to the standard \(default\) currency fields found in most applications. They are highly configurable, support use of custom rate tables, report aggregations, and provide for improved visibility into conversion calculations.

**Note:** You don't have to install a plugin to use FX Currency functionality. It's activated by default.

## Use considerations

Use the FX Currency field type in place of the standard currency fields when you must:

-   Support values expressed in multiple currencies, for example, EUR 100, JPY 200, USD 30, as values in a field. FX Currency fields provide better support for multi-currency applications than do standard currency fields.
-   Control how the FX Currency field is configured, including specifying its internal behavior and currency value formatting.

    To learn more about currency configuration, see [Configuring FX Currency field behavior](configure-fx-currency-field-behavior.md).

-   Create custom conversion rate tables.

    To learn more about custom table rates, see [Add conversion rates using a custom rate table](../task/custom-rate-table.md).

-   Have more control over when the actual currency conversion occurs. FX Currency values convert on demand only, making the conversion results much more transparent.

    To learn more about currency conversions, see [Understanding how FX Currency field conversions work](fx-currency-conversions.md).

-   Provide greater transparency into currency conversion calculations. You can view and configure the calculation components, including conversion dates, reference currency, and number of displayed decimals.
-   Build query conditions using FX Currency field values. For available query conditions, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).
-   Access FX Currency fields through richer scriptable APIs.
-   Aggregate currency values as entered by users, or aggregate them in selected reference currencies, for reporting purposes.
-   Use the three-digit ISO 4217 numeric currency code for a currency with Numeric code field on the Currency \[fx\_currency\] table and the ScriptableCurrencyCode API. For more information, see .

**Important:** You can add FX Currency fields to base and custom applications, and they work independently of existing standard currency fields. However, you can't convert or change a standard currency field to an FX Currency type field. No functions are available to convert standard currency fields to FX Currency fields, then migrate the data from one to the other.

-   **[Understanding FX Currency values in forms](fx-currency-values-forms.md)**  
In forms, the FX Currency field behaves like a dot walkable field in script. It consists of an entry field, and an accompanying list for selection of a currency code.
-   **[Understanding how FX Currency field conversions work](fx-currency-conversions.md)**  
You can use existing system currency rates or define a custom conversion rate table for use in FX Currency processing.
-   **[Understanding FX Currency values in lists and reports](fx-currency-values-lists-reports.md)**  
By default, the currency values that appear in the FX Currency fields in lists and reports are the values that you directly enter into the FX Currency fields. For reports, the aggregations of FX Currency fields are, by default, reference currency values.
-   **[FX Currency values in import and export](fx-currency-values-import-export.md)**  
In general, currency values crossing the boundaries of the platform represent whatever is returned by `getDisplayValue`. Usually this currency value is the default as entered by a user into an FX Currency field for a transaction.

**Parent Topic:**[Exploring currency administration](explore-currency-admin.md)

**Related topics**  


[Standard currency fields](configure-and-use-default-currency-fields.md)

[Field types reference](../../reference-pages/reference/r_FieldTypes.md)

