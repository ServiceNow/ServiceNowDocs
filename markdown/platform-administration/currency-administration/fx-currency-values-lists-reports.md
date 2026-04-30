---
title: Understanding FX Currency values in lists and reports
description: By default, the currency values that appear in the FX Currency fields in lists and reports are the values that you directly enter into the FX Currency fields. For reports, the aggregations of FX Currency fields are, by default, reference currency values.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [FX Currency fields, Exploring currency administration, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Understanding FX Currency values in lists and reports

By default, the currency values that appear in the FX Currency fields in lists and reports are the values that you directly enter into the FX Currency fields. For reports, the aggregations of FX Currency fields are, by default, reference currency values.

## FX Currency values in list views

In lists, FX Currency values appear as a formatted currency string returned from getDisplayValue\(\).

-   The settings in the **Display Digits** and **Display Value Currency** fields in **System Localization** &gt; **FX Currency Configuration** determine how the currency values appear in lists.
-   To learn more, see [Identify the FX Currency field and its display parameters](../task/fx-currency-display-parameters.md).

For an FX Currency field that depends on another FX Currency field, the currency value comes from the Currency Instance \[fx\_currency2\_instance\] record associated with the latter. The display value format is based on how you configured its display settings in **System Localization** &gt; **FX Currency Configuration.**

**Note:** An FX Currency field in a custom table is a reference field that stores the reference \(sys\_id\) to the actual record. Because the sys\_id is 32 characters, the **Max length** of the FX Currency column must be 32 \(default\).

## Filtering FX Currency values in lists

In lists, FX Currency field filtering behaves differently than with standard currency fields. The filtering takes place using the currency type selected when a currency value is originally entered into an FX Currency field. It doesn't take reference currencies into account when you filter a list. So, if the unfiltered list contains FX Currency field entries in multiple currencies, a filtered list would only contain those records originally entered using the specified filtering currency.

-   For example, if you entered a currency value in Euros \(EUR\) and the reference currency is US Dollars \(USD\), the reference currency value may appear in an unfiltered list.
-   However, if you filter the list, and select USD as the currency, the currency value, originally entered in Euros, doesn't appear. In this case, only currency values originally entered in USD would appear.

## Dependent FX Currency fields

Use of FX Currency view or dependent fields enable you to use alternate display configurations defined in **System Localization** &gt; **FX Currency Configuration** for a particular FX Currency field. To learn more about FX Currency field configurations, see [Configuring FX Currency field behavior](configure-fx-currency-field-behavior.md).

When you create an FX Currency field, you can mark it as dependent on another FX Currency field. Marking an FX Currency field as dependent enables it to use the configuration settings for the original FX Currency field to display the amount values in different currency. Any changes that you make to the dependent field don't affect the original FX Currency field.

## FX Currency reporting, aggregation, and group by

You can select FX Currency fields for inclusion on reports, and they display in the same manner as in list views.

-   FX Currency fields appear as a formatted currency string returned from getDisplayValue\(\).
-   If you set the **Display Value Currency** field in **System Localization** &gt; **All Properties** to **Display in Session Currency**, the session currency assigned to the user running the report appears.

You can aggregate like reference currency values within a Currency Instance record. The following is the aggregated FX Currency data format in the ServiceNow AI Platform®:

<table id="table_wnw_24t_1mb"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Value of the aggregation. If the values being aggregated are FX Currency values, the returned value is in the format `currency_code:currency_value`, such as:`USD:134.980000`

 Otherwise, the returned value is just the currency value, such as: `134.980000`.

**Note:** If the field contains FX Currency values of mixed currency types, the values cannot be aggregated. The value is returned as a semicolon \(;\).

</td></tr></tbody>
</table>For example, if the **Cost** field on a transaction record is an FX Currency field, you can group by **cost.amount** or **cost.currency**.

-   Aggregation operations, such as SUM, translate as `SUM(amount)` or `SUM(reference_amount)`. The aggregation source determines the translation when the currency associated with the currency values in the grouping is the same.

    For example, the aggregate value returned by `GlideAggregate.getAggregate()` is a string of the format USD; 1234.56. The total currency value is expressed in the single reference currency that is associated with all currency values in the grouping.

-   If there are different currencies associated with currency values in the grouping, then the aggregate value is empty. For example, if some of the currency values are in US Dollars, some are in Euros, and others in Yen, the aggregate value would be empty.

You can also use a Group By command on FX Currency fields.

-   It is equivalent to grouping by currency and amount, or by reference\_currency and reference\_amount, as dictated by the aggregation source.
-   The value of the grouping is available by dot-walking on the FX Currency field, or using an API such as `getDisplayValue()`.

**Parent Topic:**[FX Currency fields](fx-currency.md)

**Related topics**  


[Configuring FX Currency global settings](../task/fx-currency-configure.md)

[Configuring FX Currency field behavior](configure-fx-currency-field-behavior.md)

