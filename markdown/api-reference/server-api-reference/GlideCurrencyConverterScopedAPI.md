---
title: GlideCurrencyConverter - Scoped
description: The GlideCurrencyConverter API provides methods to convert one currency value to another, such as converting US dollars into European euros.Instantiates a GlideCurrencyConverter object.Instantiates a GlideCurrencyConverter object and sets the source and destination country codes to use in the currency conversion.Executes the currency converter.Sets the amount of currency to convert.Sets the currency conversion date and time.Sets the country code of the source currency.Defines the rate table to use in the currency conversion.Sets the country code of the destination currency.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencyConverter- Scoped

The GlideCurrencyConverter API provides methods to convert one currency value to another, such as converting US dollars into European euros.

You can instantiate the GlideCurrencyConverter object and define the source and destination currencies during instantiation using GlideCurrencyConverter\(from, to\). You can also instantiate the object without these values and define them later using the setFromCurrency\(\) and setToCurrency\(\) methods. These values and the amount to convert must be set before calling the convert\(\) method to perform the currency conversion. To set the amount to convert, use the setAmount\(\) method.

The GlideCurrencyConverter\(\) API also provides optional methods that enable you to:

-   Set the date and time for which to perform the conversion, setDateTime\(\). By setting the date and time, the rate that is used in the conversion calculation is that for the specified date and time, instead of the default of the current date and time.
-   Set the rate table to use in the conversion, setRateTable\(\). By default the conversion uses the fx\_system\_rate table however, you can define custom rate tables for your instance. For additional information on creating rate tables, see [Add conversion rates using a custom rate table](https://www.servicenow.com/docs/access?context=custom-rate-table&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

This class runs is in the `sn_currency` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencyConverter - GlideCurrencyConverter\(\)

Instantiates a GlideCurrencyConverter object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

This example shows how to call the method.

```api-constructor
var conv = new sn_currency.GlideCurrencyConverter();
```

## GlideCurrencyConverter - GlideCurrencyConverter\(String from, String to\)

Instantiates a GlideCurrencyConverter object and sets the source and destination country codes to use in the currency conversion.

|Name|Type|Description|
|----|----|-----------|
|from|String|Three-letter ISO 3166 country code of the source currency.|
|to|String|Three-letter ISO 3166 country code of the converted currency.|

This example shows how to call the method.

```api-constructor
var conv = new sn_currency.GlideCurrencyConverter('EUR', 'USD');
```

## GlideCurrencyConverter - convert\(\)

Executes the currency converter.

Call this method after calling other GlideCurrencyConverter methods that construct the currency conversion, such as setAmount\(\), setRateTable\(\), and setDate\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ryh_2hq_cy" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

If the conversion is successful, returns CurrencyExchangeValue object. If unsuccessful, returns "null".```
CurrencyExchangeValue {
Rate: Number,
OriginalAmount: Number,
Amount: Number,
fromCurrency: String,
toCurrency: String,
rateSysId: String
}
```

 **Rate**: Number. Exchange rate used in the conversion.

 **OriginalAmount**: Number. Source currency amount.

 **Amount**: Number. Converted amount \(**OriginalAmount** \* **Rate**\).

 **fromCurrency**: String. Three-letter ISO 3166 country code of the source currency.

 **toCurrency**: String. Three-letter ISO 3166 country code of the converted currency.

 **rateSysId**: String. Sys\_id of the rate table record used to calculate the conversion.

</td></tr></tbody>
</table>This example shows how to call the method.

```
var conv = new sn_currency.GlideCurrencyConverter('EUR', 'USD');
conv.setAmount(100);
gs.info(conv.convert());
```

Output:

```
CurrencyExchangeValue{Rate = 1.0777, OriginalAmount = 100, Amount = 107.7700, fromCurrency = 'EUR', toCurrency = 'USD', rateSysId = '2ed537fcb271937adb'}
```

## GlideCurrencyConverter - setAmount\(String amount\)

Sets the amount of currency to convert.

|Name|Type|Description|
|----|----|-----------|
|amount|String|Currency amount to convert. This value must be unformatted except for a decimal point to denote fractional currency. For example, 1234.56 is valid, 1,234.56 is invalid.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var conv = new sn_currency.GlideCurrencyConverter('EUR', 'USD');
conv.setAmount(100);
```

## GlideCurrencyConverter - setDateTime\(Object date\)

Sets the currency conversion date and time.

This date and time determines the conversion rate that is used to convert the currency. If this method is not called before the GlideCurrencyConverter.convert\(\) method, the conversion is performed using the rate for the current date/time.

|Name|Type|Description|
|----|----|-----------|
|date|GlideDateTime|Date/time for which to calculate the currency conversion. This value determines the rate that is used in the conversion.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to call this method.

```
var conv = new sn_currency.GlideCurrencyConverter('EUR', 'USD');
conv.setAmount(100);
var gd = new GlideDateTime("2019-01-03 11:00:00");
conv.setDateTime(gd);
gs.info(conv.convert());
```

Output:

```
CurrencyExchangeValue{fOriginalAmount=100, fOriginalCurrency='EUR', fRate=1.061, fAmount=106.1, fCurrency='USD', fRateSysId='4555525f5553445f3130303030313031'}
```

## GlideCurrencyConverter - setFromCurrency\(String from\)

Sets the country code of the source currency.

|Name|Type|Description|
|----|----|-----------|
|from|String|Three-letter ISO 3166 country code of the source currency.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var conv = new sn_currency.GlideCurrencyConverter().setFromCurrency('FRA');
```

## GlideCurrencyConverter - setRateTable\(String rateTable\)

Defines the rate table to use in the currency conversion.

If this method is not called before the GlideCurrencyConverter.convert\(\) method is called, the conversion is performed using the fx\_system\_rate table. All custom rate tables must extend the fx\_conversion\_rate table. For additional information on creating rate tables, see [Add conversion rates using a custom rate table](https://www.servicenow.com/docs/access?context=custom-rate-table&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|rateTable|String|Name of the rate table to use in the currency conversion.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var conv = new sn_currency.GlideCurrencyConverter('EUR', 'USD');
conv.setRateTable(custom_rate_table);
```

## GlideCurrencyConverter - setToCurrency\(String to\)

Sets the country code of the destination currency.

|Name|Type|Description|
|----|----|-----------|
|to|String|Three-letter ISO 3166 country code of the source currency.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var conv = new sn_currency.GlideCurrencyConverter().setToCurrency('USA');
```

