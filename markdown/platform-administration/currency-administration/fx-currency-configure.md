---
title: Configuring FX Currency global settings
description: Before setting up and using FX Currency, review the related system properties to confirm or modify its default behavior.
locale: en-US
release: xanadu
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up defaults required for FX Currency use, Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring FX Currency global settings

Before setting up and using FX Currency, review the related system properties to confirm or modify its default behavior.

## Before you begin

Role required: admin

## About this task

The global defaults you establish in system properties apply the configuration option to all FX Currency fields. You can then customize them for specific dictionary attributes in **System Localization** &gt; **FX Currency Configuration.** When you create a currency configuration, it applies those settings only to the FX Currency field that you add it to. To learn more about FX Currency configurations, see [Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md).

FX Currency configuration settings for specific FX Currency fields take precedence over system properties. Administrators can set a global configuration for a property, and then apply exceptions on a field-by-field basis.

-   If you change system defaults, except for **display\_digits** and **display\_value**, the changes apply to updated and new values only.
-   Existing values and data don't change but rather display differently, depending on configuration.

**Important:** Don't edit the Currency \[fx\_currency\] table directly. The system maintains this table and your changes could have unintended consequences.

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **FX Currency Configuration.**

2.  Review the system defaults and make any desired changes.

<table id="table_j32_npz_xjb"><thead><tr><th>

System property

</th><th>

FX Currency configuration mapping

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.currency2.display\_digits

</td><td>

currency\_display\_digits

</td><td>

Default number of digits displayed in FX Currency fields. **Note:** In a form, FX Currency fields display the number of digits you enter, up to 12 digits in length.

 -   **Type**: Number
-   **Default value**: -1, or currency default
-   **Available options**: 0–12
-   **Develop**: [GlideCurrencyFormatter](https://developer.servicenow.com/go_to_api.do?ID=GlideCurrencyFormatterScopedAPI&v=kingston)


</td></tr><tr><td>

glide.currency2.display\_value

</td><td>

currency\_display\_value

</td><td>

Default currency display value returned from getDisplayValue\(\).-   **Type**: String
-   **Default value**: as\_entered
-   **Available options**:
    -   as\_entered: Currency value as entered by the user
    -   in\_session\_currency: Currency value as entered by the user and converted to the session currency
    -   in\_reference\_currency: Currency value as entered by the user converted to the reference currency
-   **Develop**: [GlideCurrencyFormatter](https://developer.servicenow.com/go_to_api.do?ID=GlideCurrencyFormatterScopedAPI&v=kingston)


</td></tr><tr><td>

glide.currency2.system\_rate\_table

</td><td>

conversion\_rate\_table

</td><td>

Conversion rate table used to perform currency conversions. By default, the source for currency conversions is the System Currency Conversion Rate \[fx\_system\_rate\] table, which stores the daily reference rates retrieved from the European Central Bank. If you have defined a custom rate table, you can change the rate table used in currency conversions. -   **Type**: String
-   **Default value**: fx\_system\_rate
-   **Available options**: Any table that extends the **Currency Conversion Rate** table \[fx\_conversion\_rate\]
-   **Learn more**: [Understanding how FX Currency field conversions work](../concept/fx-currency-conversions.md)and [Default currency conversions](../concept/currency-conversions.md)
-   **Develop**: [GlideCurrencyConverter](https://developer.servicenow.com/go_to_api.do?ID=GlideCurrencyConverterScopedAPI&v=kingston) [GlideCurrencyExchangeValue](https://developer.servicenow.com/go_to_api.do?ID=GlideCurrencyExchangeValueScopedAPI&v=kingston)


</td></tr><tr><td>

glide.currency2.default\_reference\_currency

</td><td>

reference\_currency

</td><td>

Three-digit ISO currency code used for the reference currency. The default reference currency for FX Currency fields is the system reference currency.-   **Type**: String
-   **Default value**: If you set **glide.system.reference\_currency** to true, the three-digit ISO currency code determined by **glide.system.reference\_currency.code**.

If set to false, the system locale is the default.

-   **Learn more**: [Session and reference currency](../concept/session-and-reference-currency.md)
-   **Develop**: [GlideElementCurrency2](https://developer.servicenow.com/go_to_api.do?ID=GlideElementCurrency2API&v=kingston)


</td></tr></tbody>
</table>
**Parent Topic:**[Setting up defaults required for FX Currency use](../concept/setting-up-defaults-fx-currency-use.md)

**Related topics**  


[Add conversion rates using a custom rate table](custom-rate-table.md)

[Add an FX Currency field to a table](add-fx-currency-field-table.md)

[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

[Updating the Currency Instance record](updating-fx-currency-instance-record.md)

