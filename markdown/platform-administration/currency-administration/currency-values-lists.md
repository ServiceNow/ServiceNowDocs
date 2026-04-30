---
title: Default currency values in lists
description: In lists, default currency values appear in the user’s session currency, formatted for display in the user’s locale. Typically, a formatted number follows the currency symbol.
locale: en-US
release: xanadu
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Standard currency fields, Exploring currency administration, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Default currency values in lists

In lists, default currency values appear in the user’s session currency, formatted for display in the user’s locale. Typically, a formatted number follows the currency symbol.

Different field types appear as follows in lists:

<table id="table_b1r_nnk_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Currency field type

</td><td>

Value expressed in the user’s session currency.

</td></tr><tr><td>

Price field type

</td><td>

-   **Calculated**: Value in the user’s session currency.
-   **Fixed**: Currency value, as entered by the user.
-   **Multiple**: Value associated with the user’s session currency if this value exists. Otherwise, the first value entered converts to the user’s session currency.

</td></tr></tbody>
</table>A Globe icon appears beside the currency value that enables you change to one of the following values:

-   Value as entered by the user.
-   Value in session currency.
-   Value as entered and, in brackets, the value in reference currency.

The icon appears when the user’s session currency is different from the currency entered. Clicking the icon cycles through the listed displays. In the preview for the record, currency values appear as entered, formatted in the user’s locale.

## Aggregation

Aggregation operations can be used on currency columns. Aggregation operations include total, group by, average, minimum, and maximum. Aggregation is done in two steps:

-   Aggregate the reference currency values for all records.
-   Convert this aggregate to the user’s session currency for display.

**Note:** The resulting value may not be what you expect. The conversion rate used for the value that appears for the currency field, and for its reference currency, that is used for the aggregation, may have changed.

This limitation extends to different price types.

-   For price type fixed, the calculated reference value can be old.
-   For price type multiple, the reference value of the first price entered is used. The other values are not used.

The aggregate value is shown formatted in user’s locale with a currency symbol. Currency fields are stored with four decimal places, and aggregates have four decimal places. For upgrades, you must set the **glide.currency\_price.use\_all\_fraction\_digits** property. See [Change default currency decimal places](../task/change-currency-fraction-digits.md) for more information.

## Filtering

You can set up filters on currency fields. The currency value is entered as a currency code and numeric value. Filtering is done in two steps:

-   The filter currency value is converted to the reference currency.
-   The filter’s calculated reference value is compared with the reference value in the records.

Matching records are shown in the list view.

**Note:** At times, the filtering results might not provide the expected result. The conversion rate used when you run the filter might be different than the conversion rate used when calculating the reference values in the individual records. This limitation extends to the following price types:

-   For a Fixed price field type, the calculated reference value can be old.
-   For a Multiple price field type, it uses the reference value of the first price, and does not use the other values.

**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

