---
title: Default currency values in scripts
description: You can use currency fields in scripts.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Standard currency fields, Explore, Currency administration, Configure core features, Administer]
---

# Default currency values in scripts

You can use currency fields in scripts.

These methods are available on GlideElement objects.

To display currency values, use the getDisplayValue\(\) display API. To work with currency values in any way other than display, use the APIs that return/accept unformatted numbers.

**Note:** Before performing calculations on the value, do not use the getDisplayValue\(\) methods and then process the string to remove formatting information.

Methods such as getValue\(\) and getCurrencyValue\(\) return unformatted numbers as strings. To obtain the floating point value, use the JavaScript function parseFloat\(\), and then use resulting value to perform calculations. To obtain the currency associated with these values, use the APIs that return the currency code. You can also use the getCurrencyCode\(\) methods to determine a field's currency.

```
var rate = parseFloat(current.base_rate);
var currencyCode = current.base_rate.getCurrencyCode();

```

Use the setValue\(\) method to set the value of a currency field. If this currency is the user’s session currency, use a plain number or the floating point number of a string containing it. Otherwise, prefix the value with the 3-letter ISO currency code.

```
var totalCost = rate*current.hourly_rate;
current.total_cost.setValue(currencyCode + ";" + totalCost);

```

You are working with the reference currency value when you use GlideAggregate on currency or price fields. Be sure to convert the aggregate values to the user's session currency for display. The resulting value may not be what you expect. The conversion rate used for the currency or price field value, and for its reference currency, which is used for the aggregation, may have changed.

When you delete a record containing a currency value, the platform deletes any associated currency records.

**Note:** Do not use deleteMultiple\(\) on tables with currency fields. Always delete each record individually.

Currency values contain four decimal places.

-   APIs that return values such as getValue\(\) return up to four decimal places. Trailing zeros are always removed.
-   APIs that return display values such as getDisplayValue\(\) have at least two decimal places and up to four decimal places.
-   GlideAggregate returns four decimal places.

You can have the system use two decimal places. When you set it to two decimal places, numeric values returned by the API contain two decimal places. Although currency conversion rates may have more decimal places, currency fields store only two decimal places. APIs that accept numeric values round decimal places to two places.

-   APIs that return values such as getValue\(\) return up to two decimal places. The trailing zeroes are removed for values read from the database, but if a value such as 00 is set later, 1.00 can be returned. The number of trailing zeros returned is not consistent.
-   APIs that return display values such as getDisplayValue\(\) contain up to two decimal places. It could sometimes return two places even for values such as 7.10, but could remove trailing zeros at other times. The number of trailing zeros returned is not consistent.
-   GlideAggregate returns two decimal places.

**Note:** To learn how to change the number of decimal places used by the system, see [Change default currency decimal places](../task/change-currency-fraction-digits.md).

The following example, the user’s locale is set to German \(de.DE\), and the reference currency set to USD. The values use a currency value of 21345.67 in Japanese yen, 1563.72 in Euros, and 1152.48 in US dollars.

<table id="table_crh_3kb_hx"><thead><tr><th>

Method name

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

getValue\(\)

</td><td>

Returns the currency value in the user's session currency as an unformatted number.

</td><td>

1563.72

</td></tr><tr><td>

getReferenceValue\(\)

</td><td>

Returns the currency value in the reference currency as an unformatted number.

</td><td>

1152.48

</td></tr><tr><td>

getSessionValue\(\)

</td><td>

Returns the currency value in the user's session currency as and unformatted number.

</td><td>

1563.72

</td></tr><tr><td>

getCurrencyValue\(\)

</td><td>

Returns the currency value as entered as an unformatted number.

</td><td>

21345.67

</td></tr><tr><td>

getDisplayValue\(\)

</td><td>

Returns the currency value in the user's session currency, formatted in the user's locale with a currency symbol.

</td><td>

€1.563,72

</td></tr><tr><td>

getSessionDisplayValue\(\)

</td><td>

Returns the currency value in the user's session currency, formatted in the user's locale with a currency symbol.

</td><td>

€1.563,72

</td></tr><tr><td>

getReferenceDisplayValue\(\)

</td><td>

Returns the currency value in the reference currency, formatted in the user's locale with a currency symbol.

</td><td>

$1,152.48

</td></tr><tr><td>

getCurrencyDisplayValue\(\)

</td><td>

Returns the currency value as entered formatted in the user's locale with a currency symbol.

</td><td>

¥21.345,67

</td></tr><tr><td>

getCurrencyString\(\)

</td><td>

Returns the currency value as entered as an unformatted number, prefixed by the 3-letter ISO currency code, separated by a semicolon.

</td><td>

JPY 21345.67

</td></tr><tr><td>

getCurrencyCode\(\)

</td><td>

Returns the 3-letter ISO currency code for the currency value as entered.

</td><td>

JPY

</td></tr><tr><td>

getSessionCurrencyCode\(\)

</td><td>

Returns the 3-letter ISO currency code for the user's session currency.

</td><td>

EUR

</td></tr><tr><td>

getReferenceCurrencyCode\(\)

</td><td>

Returns the 3-letter ISO currency code for the reference currency.

</td><td>

USD

</td></tr><tr><td>

setValue\(\)

</td><td>

Sets the currency value as:-   An unformatted number taken as a value in the user's session currency.
-   An unformatted number prefixed by a 3-letter currency code separated by a semicolon.

</td><td>

4369.21 or JPY 4369.21

</td></tr><tr><td>

setDisplayValue\(\)

</td><td>

Sets the currency value as:-   A number formatted in the user's locale that is taken as a value in the user's session currency.
-   A number formatted in the user's locale prefixed by a 3-letter currency code separated by a semicolon.

</td><td>

4369.21 or JPY 4369.21

</td></tr></tbody>
</table>**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

