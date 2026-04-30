---
title: Add conversion rates using a custom rate table
description: You can create a custom rate table to ensure repeatable and consistent calculations. In a custom rate table, you control the conversion rates and the frequency of rate conversions. If you don't define custom rate tables, FX Currency fields use the System Conversion Currency Rate \[fx\_system\_rate\] table, which updates rates daily from the ECB \(European Central Bank\) website.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Defaults required for FX Currency use, Configure, Currency administration, Configure core features, Administer]
---

# Add conversion rates using a custom rate table

You can create a custom rate table to ensure repeatable and consistent calculations. In a custom rate table, you control the conversion rates and the frequency of rate conversions. If you don't define custom rate tables, FX Currency fields use the System Conversion Currency Rate \[fx\_system\_rate\] table, which updates rates daily from the ECB \(European Central Bank\) website.

## Before you begin

Role required: admin, currency\_admin

## About this task

A conversion rate can be quoted in different ways.

-   Direct conversion rate \(A -&gt; B\) that may or not be invertible \(that is, given rate R for A -&gt; B, the rate for B -&gt; A can be derived as 1/R\).
-   Indirect conversion rate through some intermediate currency \(A -&gt; C and C -&gt; B\).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Click **New**.

3.  In **Label** field, enter the name of the conversation rate.

    For example, Convert-US-Euro.

4.  In the **Extends** field, select the Currency Conversion Rate \[fx\_conversion\_rate\] table.

5.  Complete the remaining fields to create the new extended table.

    For more details, see [Create a table](../../table-administration/task/t_CreateATable.md) for details.

6.  Click **Submit**.

7.  Navigate to the new table and fill in the fields on the form.

<table id="table_vyx_ygm_4jb"><thead><tr><th>

**Field**

</th><th>

**Description**

</th></tr></thead><tbody><tr><td>

From Currency

</td><td>

Currency to convert the rate conversion table from. For example, USD if you are converting from US Dollars.

</td></tr><tr><td>

To Currency

</td><td>

Currency to convert the rate conversion table to. For example, EUR if you are converting to Euros.

</td></tr><tr><td>

Span start

</td><td>

Date/time from which this currency rate is valid, for example, January 1, 2020 00:00:00.

</td></tr><tr><td>

Span end

</td><td>

Date/time to which this currency rate is valid, for example, January 30, 2020 23:59:59.

</td></tr><tr><td>

Order

</td><td>

Order in which a currency conversion selects currency rates when their time spans overlap.

 For a date/time and a currency pair, if there are multiple rates with a Span start less than or equal to the date/time, and Span end greater than or equal to the date/ time, the currency conversion selects the lowest order rate.

</td></tr><tr><td>

Rate

</td><td>

Actual conversion rate, stored as a decimal with six decimal places.

</td></tr></tbody>
</table>8.  Click **Update**.


## What to do next

After you create the custom rate table:

1.  Manually populate the table, or import data to populate it.
2.  To use this rate table on a global basis, change the **glide.currency2.system\_rate\_table** system property.

    To use it for a specific FX Currency field, change the **Conversion Rate Table** field setting in **System Localization** &gt; **FX Currency Configuration.**


**Parent Topic:**[Setting up defaults required for FX Currency use](../concept/setting-up-defaults-fx-currency-use.md)

**Related topics**  


[Configuring FX Currency global settings](fx-currency-configure.md)

[Add an FX Currency field to a table](add-fx-currency-field-table.md)

[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

[Update a Currency Instance record](updating-fx-currency-instance-record.md)

[FX Currency values in import and export](../concept/fx-currency-values-import-export.md)

[Configuring FX Currency global settings](fx-currency-configure.md)

[Specify the rate table and date source for currency conversions](fx-currency-conv-rate-table-date-source.md)

