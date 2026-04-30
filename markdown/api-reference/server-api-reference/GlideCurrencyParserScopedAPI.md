---
title: GlideCurrencyParser - Scoped
description: The GlideCurrencyParser API provides methods to parse FX Currency values to detect locale-based formatting.Instantiates a GlideCurrencyParser object that provides methods to parse a string into a GlideCurrencyValue object.Parses a specified string into a GlideCurrencyValue object to obtain locale-based currency formatting.Sets the currency code for the associated GlideCurrencyParser object.Sets the default language and country codes, which constitute the locale, on the associated GlideCurrencyParser object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencyParser- Scoped

The GlideCurrencyParser API provides methods to parse FX Currency values to detect locale-based formatting.

The methods in this class parse a specified string into a [GlideCurrencyValue](../../GlideCurrencyValue/concept/GlideCurrencyValueScopedAPI.md#) object enabling you to obtain locale-based currency formatting. Before calling the GlideCurrencyParser.parse\(\) method, which actually performs the parse, you must set the currency code to use during the parse. You can set the currency code by either passing it in the GlideCurrencyParser.parse\(\) method call or by calling GlideCurrencyParser.setDefaultCurrencyCode\(\).

Setting the locale is optional. If you do not set it through the GlideCurrencyParser.setLocale\(\) method, the currency amount passed into GlideCurrencyParser.parse\(\) must be unformatted.

This API is provided within the `sn_currency` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencyParser - GlideCurrencyParser\(\)

Instantiates a GlideCurrencyParser object that provides methods to parse a string into a GlideCurrencyValue object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

This example shows how to call the method.

```api-constructor
var parser = new sn_currency.GlideCurrencyParser();
```

## GlideCurrencyParser - parse\(String value\)

Parses a specified string into a GlideCurrencyValue object to obtain locale-based currency formatting.

<table id="table_wpy_532_4jb" class="parameters"><thead><tr><th>

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

String to parse. You can prepend this string with the ISO currency code to use when parsing the string \(semicolon separated\). If the currency code is not set prior to calling the parse\(\) method, it defaults to the current session currency code.This method supports both decimal point and decimal comma notation.

 For example: "123.45", "USD;123.45", "123,45", "EUR;123,45"

</td></tr></tbody>
</table><table id="table_xpy_532_4jb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideCurrencyValue

</td><td>

Parsed value information.Data type: Object

</td></tr></tbody>
</table>This example sets the locale to France and then parses the passed currency value to US dollars.

```
var gp = new sn_currency.GlideCurrencyParser();
gp.setLocale("fr", "FR");
var cv = gp.parse("USD;1234,56");
gs.info(cv);
```

Output:

```
USD;1234.56
```

This example sets the default currency code to US dollars and then parses the currency value.

```
var amount = "1234.56"
var gp = new sn_currency.GlideCurrencyParser();
gp.setDefaultCurrencyCode("USD");
var cv = gp.parse(amount);
gs.info(cv);
```

Output:

```
USD;1234.56
```

## GlideCurrencyParser - setDefaultCurrencyCode\(String currencyCode\)

Sets the currency code for the associated GlideCurrencyParser object.

|Name|Type|Description|
|----|----|-----------|
|currencyCode|String|Three-letter ISO currency code to use as the default in the associated GlideCurrencyParser object.|

|Type|Description|
|----|-----------|
|void| |

The following example sets the default currency code to US dollars.

```
var amount = "123.45"
var gp = new sn_currency.GlideCurrencyParser();
gp.setDefaultCurrencyCode("USD");
var cv = gp.parse(amount);
gs.info(cv);
```

Output:

```
USD;123.45
```

## GlideCurrencyParser - setLocale\(String language, String country\)

Sets the default language and country codes, which constitute the locale, on the associated GlideCurrencyParser object.

If you do not call this method before calling the GlideCurrencyParser.parse\(\) method, the locale defaults to the current session locale.

|Name|Type|Description|
|----|----|-----------|
|language|String|Two-letter ISO 639 language code, such as en, es, and fr.|
|country|String|Two-letter ISO 3166 country code, such as US, ES, and FR.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to set the locale to Spain.

```
var amount = "USD;1.234,56"
var gp = new sn_currency.GlideCurrencyParser();
gp.setLocale("es", "ES");
var cv = gp.parse(amount);
gs.info(cv);
```

Output:

```
USD;1234.56
```

