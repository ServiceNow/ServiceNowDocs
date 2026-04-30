---
title: Specify the rate table and date source for currency conversions
description: Identify the rate table and data source to use for currency conversions for the designated FX Currency field.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [FX Currency field behavior, Defaults required for FX Currency use, Configure, Currency administration, Configure core features, Administer]
---

# Specify the rate table and date source for currency conversions

Identify the rate table and data source to use for currency conversions for the designated FX Currency field.

## Procedure

1.  Click the Rate Table tab.

2.  In the **Conversion Rate Table** field, select the rate table used for conversions of currency values in the FX Currency field:

    -   To use the default system rate table you defined in the **glide.currency2.system\_rate\_table** property in **System Localization** &gt; **All Properties.**, select **System Currency Conversion Rate**. This table stores daily reference rates retrieved from the European Central Bank.

        To learn more about the system rate table, see [Default currency conversions](../concept/currency-conversions.md).

    -   If you have defined a custom rate table, you can select it to use in currency conversions for the FX Currency field. To learn more about how to define custom rate tables, see [Add conversion rates using a custom rate table](custom-rate-table.md).
3.  In the **Conversion Date Source** field, select the field to use as the source of the date and time for the currency conversion for the FX Currency field:

    -   To use the date and time at which the user performs the currency conversion, select **--None--**.
    -   To use as the source of the date and time for the currency conversion, select the dot-walked field.

        For example, to perform the currency conversion based on the currency rates in effect, select a transaction date field. So, if you entered the transaction on July 15, and you perform the currency conversion on July 31, it uses the currency conversion rates in effect on July 15.

4.  Click **Save**.


**Parent Topic:**[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

**Related topics**  


[Understanding how FX Currency field conversions work](../concept/fx-currency-conversions.md)

[Add conversion rates using a custom rate table](custom-rate-table.md)

