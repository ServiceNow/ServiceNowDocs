---
title: GlideCurrencyFormatter - Scoped
description: The GlideCurrencyFormatter API provides methods to format FX Currency strings.Instantiates a GlideCurrencyFormatter object and defines the format string to use to format FX Currency.Formats a specified currency value using the specified currency code.Sets the default language and country, which constitutes the locale, for the currency formatter.Sets the maximum number of digits to the right of the decimal point/decimal comma to return.Sets the minimum number of fraction digits \(right of the decimal point/decimal comma\) to return.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencyFormatter- Scoped

The GlideCurrencyFormatter API provides methods to format FX Currency strings.

When instantiating the GlideCurrencyFormatter object, you define the format of the output results for this object. Once set, the same format is used each time you call the GlideCurrencyFormatter.format\(\) method of that object. The GlideCurrencyFormatter\(\) and format\(\) methods are the only two methods that you must call to format FX Currency.

The GlideCurrencyFormatter\(\) API also provides optional methods that enable you to:

-   Set the locale of the currency using setLocale\(\). By setting the locale, the formatter takes into consideration any formatting that is specific to that locale, such as whether a decimal point or decimal comma is used to denote fractions of currency amount. Default: System locale
-   Set the minimum number of fractional digits to display using setMinFractionDigits\(\). Defines the minimum number of digits to the right of the decimal point/decimal comma to include. By default, all digits passed in are displayed. If the passed in amount has fewer digits than the specified minimum, the result is padded with "0".
-   Set the maximum number of fractional digits to display using setMaxFractionDigits\(\). Defines the maximum number of digits to the right of the decimal point/decimal comma to include. By default, all digits passed in are displayed. If the passed in amount has a greater number of digits than the specified maximum, the additional digits are truncated during the process of rounding to the number of maximum fraction digits. Rounding is performed to the closest right-most digit. For example, if the maximum fraction digit is set to 2 and the passed in currency value is 123.456, the formatted value is 123.46. If the currency value is 23.122, the formatted value is 23.12. If the maximum is set to less than the minimum, the minimum value is used.

This class runs is in the `sn_currency` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencyFormatter - GlideCurrencyFormatter\(String formatString\)

Instantiates a GlideCurrencyFormatter object and defines the format string to use to format FX Currency.

This method does not perform the actual string format. You must call the GlideCurrencyFormatter.format\(\) method to format the currency.

<table id="table_g3b_vbc_fy" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

formatString

</td><td>

String

</td><td>

Optional. Format string to use to format any currency passed into the formatter.Valid values:

 -   %s: Replaced by the currency symbol associated with the country code specified in the format\(\) call.
-   %v: Replaced by the currency amount, such as 123.45.
-   %c: Replaced by the ISO currency code specified in the format\(\) call, such as USD or EUR.
-   %l: Replaced with the passed in value, no formatting performed.
-   %p: Replaced by the percent sign \(%\).

 For example, if the format string is '%s%v%c' and the value to format is 123.45 in US dollars, the returned formatted string is $123.45 USD. If the format string is '%s%l%c' and the value string to format is '56M' in Euros, the returned formatted string is €56M EUR.

 **Note:** The same format string is used each time the format\(\) method is called on this object.

</td></tr></tbody>
</table>This example shows how to call the method.

```
var formatString = '%s%v%c';
var exchangeValue = new sn_currency.GlideCurrencyFormatter(formatString);
```

## GlideCurrencyFormatter - format\(String value, String currencyCode\)

Formats a specified currency value using the specified currency code.

The resulting format of the currency is also dependent on the values passed in when the GlideCurrencyFormatter object was initially instantiated.

<table id="table_hxs_f4c_fy" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

value

</td><td>

String

</td><td>

Currency amount to format. The amount can only contain a decimal point to denote the fractional amount, commas are not supported. Valid values: 123.45 or 2436.23

 Invalid values 123,45 or 2,134.56

</td></tr><tr><td>

currencyCode

</td><td>

String

</td><td>

Three-letter ISO currency code to use when formatting the currency.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Formatted currency value.|

This example shows how to call the method.

```
var amount = '123456.123456789';
var currencyCode = 'USD';
var formatString = '%s%v%c';
var exchangeValue = new sn_currency.GlideCurrencyFormatter(formatString);
gs.info('Formatted currency: ' + exchangeValue.setMaxFractionDigits(2).format(amount, currencyCode));
```

Output:

```
Formatted currency: $123,456.12USD
```

## GlideCurrencyFormatter - setLocale\(String language, String country\)

Sets the default language and country, which constitutes the locale, for the currency formatter.

If you do not call this method before calling the GlideCurrencyFormatter.format\(\) method, the locale defaults to the current session locale.

|Name|Type|Description|
|----|----|-----------|
|language|String|Two-letter ISO 639 language code, such as en, sp, and fr.|
|country|String|Two-letter ISO 3166 country code, such as US, ES, and FR.|

|Type|Description|
|----|-----------|
|void| |

This example shows setting the currency formatter to France.

```
var amount = '123456.123456789';
var currencyCode = 'EUR';
var formatString = '%s%v%c';
var exchangeValue = new sn_currency.GlideCurrencyFormatter(formatString);
exchangeValue.setLocale("fr", "FR"); // Language = fr Country = FR
gs.info('Formatted currency: ' + exchangeValue.setMaxFractionDigits(2).format(amount, currencyCode));

```

Output:

```
Formatted currency: €123 456,12EUR
```

## GlideCurrencyFormatter - setMaxFractionDigits\(Number maxFractionDigits\)

Sets the maximum number of digits to the right of the decimal point/decimal comma to return.

|Name|Type|Description|
|----|----|-----------|
|maxFractionDigits|Number|Maximum number of fraction digits to return. If this value is set to something less than the **minFractionDigits** value, it is overridden by **minFractionDigits**.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var amount = '123456.123456789';
var currencyCode = 'USD';
var formatString = '%s%v%c';
var exchangeValue = new sn_currency.GlideCurrencyFormatter(formatString);
gs.info('Formatted currency: ' + exchangeValue.setMaxFractionDigits(2).format(amount, currencyCode));
```

Output:

```
Formatted currency: $123,456.12USD
```

## GlideCurrencyFormatter - setMinFractionDigits\(Number minFractionDigits\)

Sets the minimum number of fraction digits \(right of the decimal point/decimal comma\) to return.

|Name|Type|Description|
|----|----|-----------|
|minFractionDigits|Number|Minimum number of fraction digits to return.|

|Type|Description|
|----|-----------|
|void| |

```
var amount = '123456.12';
var currencyCode = 'USD';
var formatString = '%s%v%c';
var exchangeValue = new sn_currency.GlideCurrencyFormatter(formatString);
gs.info('Formatted currency: ' + exchangeValue.setMinFractionDigits(3).format(amount, currencyCode));
```

Output:

```
Formatted currency: $123,456.120USD
```

