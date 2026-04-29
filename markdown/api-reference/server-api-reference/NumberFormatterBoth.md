---
title: NumberFormatter - Scoped, Global
description: The NumberFormatter API includes methods that return numbers formatted according to the language of the current user.Returns a string representation of a number formatted according to the language setting of the current user.Returns a string representation of a number formatted according to the language passed as a parameter.Parses a number from a passed text string, traversing left-to-right, to extract the numeric value. It then uses the passed country and language codes to identify the locale of the number and returns the parsed number in that format.Parses and returns a number from a passed text string, traversing left-to-right, until it encounters a character that it can't parse. Parsable values include numbers and the specified grouping and decimal separators.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NumberFormatter - Scoped, Global

The NumberFormatter API includes methods that return numbers formatted according to the language of the current user.

This API is available in scoped and global apps and runs in the sn\_i18n namespace.

When formatted by language or locale, users can view numbers as expected. For example, if the locale is fr \(French\), a value provided as 100.00 returns as 100,00.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NumberFormatter – format\(Number number\)

Returns a string representation of a number formatted according to the language setting of the current user.

|Name|Type|Description|
|----|----|-----------|
|number|Number|Number of any size.|

|Type|Description|
|----|-----------|
|String|Number formatted according to the language setting of the current user.|

The following example shows the return results for a user with their language set to Spanish.

```
gs.info("Number is: " + sn_i18n.NumberFormatter.format(123456.789));
gs.info("Number is: " + sn_i18n.NumberFormatter.format(-123456.789));
```

Output:

```
Number is: 123.456,789
Number is: -123.456,789
```

## NumberFormatter – formatLang\(Number number, String language\)

Returns a string representation of a number formatted according to the language passed as a parameter.

|Name|Type|Description|
|----|----|-----------|
|number|Number|Number of any size.|
|language|String|Language tag conforming with IETF BCP-47.|

|Type|Description|
|----|-----------|
|String|Number formatted according to the language passed as a parameter.|

The following example shows output for German language setting.

```
gs.info("Number is: " + sn_i18n.NumberFormatter.formatLang(123456.789, "de-de"));
gs.info("Number is: " + sn_i18n.NumberFormatter.formatLang(-123456.789, "de-de"));
```

Output:

```
Number is: 123.456,789
Number is: -123.456,789
```

## NumberFormatter - parseWithLocale\(String number, String language, String country\)

Parses a number from a passed text string, traversing left-to-right, to extract the numeric value. It then uses the passed country and language codes to identify the locale of the number and returns the parsed number in that format.

This method parses the string until it reaches a character that it doesn't recognize as a numeric value or a currency separator.

|Name|Type|Description|
|----|----|-----------|
|number|String|String to parse. This string can contain numeric values and currency separators such as commas and decimal points. For example: `"24,506.55"` or `"45.677,89"`.|
|language|String|Two-character ISO-639 language code.|
|country|String|Two-character ISO-3166 country code.|

<table id="table_imy_qgc_fbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Parsed number in the specified locale's format. Throws an exception if the first character of the string can't be parsed.

For example:

-   "123.34": Parses to 123.34 as long as the locale decimal separator is a period.
-   "1,234.56": Parses to 1234.56 as long as the locale grouping separator is a comma and the decimal separator is a period.
-   "1.234.567,89": If the grouping separator is anything but a period, parses to 1.
-   "123x456": Parses to 123.
-   "text123": Causes the method to throw a ParseException.

</td></tr></tbody>
</table>The following code example demonstrates parsing strings for various locales, as well as parsing a string with unexpected separators. The last example only partially parses the string because a space isn't a valid separator.

```
var x = sn_i18n.NumberFormatter.parseWithLocale("48,837.77", "en", "US");
var y =  sn_i18n.NumberFormatter.parseWithLocale("77.931,22", "de", "DE");
var z = sn_i18n.NumberFormatter.parseWithLocale("562 339,89", "fr", "FR");
var specialCase = sn_i18n.NumberFormatter.parseWithLocale("400 797,67", "en", "US");

gs.info(x);
gs.info(y);
gs.info(z);
gs.info(specialCase);
```

Output:

```
48837.77
77931.22
562339.89
400
```

## NumberFormatter - parseWithSeparators\(String number, String groupingSeparator, String decimalSeparator\)

Parses and returns a number from a passed text string, traversing left-to-right, until it encounters a character that it can't parse. Parsable values include numbers and the specified grouping and decimal separators.

<table id="table_o4b_rgf_gbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

number

</td><td>

String

</td><td>

String to parse. This string can contain numeric values and the specified separators such as commas and decimal points. For example: `"24,506.55"` or `"45.677,89"`.

</td></tr><tr><td>

groupingSeparator

</td><td>

String

</td><td>

Character that denotes the grouping separator, also known as the thousands separator, within the passed string. For example: Comma ",", period ".", or space " ".

</td></tr><tr><td>

decimalSeparator

</td><td>

String

</td><td>

Character that denotes the decimal separator within the passed string.For example: Comma ",", period ".", or space " ".

</td></tr></tbody>
</table><table id="table_p4b_rgf_gbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Parsed number. Throws an exception if the first character of the string can't be parsed.

For example:

-   "123.34": Parses to 123.34 as long as the locale decimal separator is a period.
-   "1,234.56": Parses to 1234.56 as long as the locale grouping separator is a comma and the decimal separator is a period.
-   "1.234.567,89": If the grouping separator is anything but a period, parses to 1.
-   "123x456": Parses to 123.
-   "text123": Causes the method to throw a ParseException.

</td></tr></tbody>
</table>The following code example shows how to parse numbers using various separators. Note that the final parse example only parses the first three digits of the number as a space is not a valid separator.

```
var x = sn_i18n.NumberFormatter.parseWithSeparators('48,837.77', ',', '.');
var y =  sn_i18n.NumberFormatter.parseWithSeparators('77.931,22', '.', ',');
var z = sn_i18n.NumberFormatter.parseWithSeparators('562 339,89', ' ', ',');
var specialCase = sn_i18n.NumberFormatter.parseWithSeparators('400 797,67', '.', ',');

gs.info(x);
gs.info(y);
gs.info(z);
gs.info(specialCase);
```

Output:

```
48837.77
77931.22
562339.89
400

```

