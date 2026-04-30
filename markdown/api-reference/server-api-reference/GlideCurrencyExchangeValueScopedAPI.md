---
title: GlideCurrencyExchangeValue - Scoped
description: The GlideCurrencyExchangeValue API provides methods to access information related to FX Currency conversions.Returns the currency amount after the conversion.Returns the converted to currency type.Returns the original, pre-conversion currency type.Returns the original, pre-conversion amount.Returns the exchange rate used during the conversion.Returns the sys\_id of the record in the rate table used in the currency conversion.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencyExchangeValue- Scoped

The GlideCurrencyExchangeValue API provides methods to access information related to FX Currency conversions.

Refer to the [GlideCurrencyConverter\(\)](../../GlideCurrencyConverter/concept/GlideCurrencyConverterScopedAPI.md#) API for methods that return a GlideCurrencyExchangeValue object.

This class runs is in the `sn_currency` namespace.

**Note:** There is no constructor for this class.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencyExchangeValue - getAmount\(\)

Returns the currency amount after the conversion.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Currency amount after the conversion.|

This example assumes a conversion rate of 1 Euro = .92 US dollars.

```
var conv = new sn_currency.GlideCurrencyConverter('EUR', 'USD');
conv.setAmount(100);
var convertValues = conv.convert();
gs.info('Exchanged Amount: ' + convertValues.getAmount());
```

Output:

```
Exchanged Amount: $92.00
```

## GlideCurrencyExchangeValue - getCurrency\(\)

Returns the converted to currency type.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Three-letter ISO currency code of the converted to currency.|

This example shows how to call the method.

```
var convertValues = new sn_currency.GlideCurrencyConverter('USD', 'JPY');
convertValues.setAmount(100);
gs.info('Exchanged Currency (To): ' + convertValues.convert().getCurrency());
```

Output:

```
Exchanged Currency (To): JPY
```

## GlideCurrancyExchangeValue - getOriginalCurrency\(\)

Returns the original, pre-conversion currency type.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Three-letter ISO currency code of the currency converted from.|

This example shows how to call the method.

```
var converter = new sn_currency.GlideCurrencyConverter('USD', 'JPY');
converter.setAmount(999.999)
var convertValues = converter.convert();
gs.info('Original Amount: ' + convertValues.getOriginalCurrency());
```

Output:

```
Original Amount: USD
```

## GlideCurrencyExchangeValue - getOriginalValue\(\)

Returns the original, pre-conversion amount.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Original amount before conversion.|

This example shows how to call the method.

```
var converter = new sn_currency.GlideCurrencyConverter('USD', 'JPY');
converter.setAmount(999.999)
var convertValues = converter.convert();
gs.info('Original Amount: ' + 'convertValues.getOriginalAmount());

```

Output:

```
Original Amount: 999.999
```

## GlideCurrencyExchangeValue - getRate\(\)

Returns the exchange rate used during the conversion.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Exchange rate used in the currency conversion.|

This example shows how to call the method.

```
var converter = new sn_currency.GlideCurrencyConverter('EUR', 'USD');
converter.setAmount(999.999)
var convertValues = converter.convert();
gs.info('Original Amount: ' + convertValues.getRate());
```

Output:

```
Exchange rate: 1.0559
```

## GlideCurrencyExchangeValue - getRateSysId\(\)

Returns the sys\_id of the record in the rate table used in the currency conversion.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the rate table used in the currency conversion.|

This example shows how to call the method.

```
var converter = new sn_currency.GlideCurrencyConverter('USD', 'JPY');
converter.setAmount(999.999)
var convertValues = converter.convert();
gs.info('Rate table sys_id: ' + convertValues.getRateSysId());
```

Output:

```
Original Amount: 99ebb4156fa831005be8883e6b3ee4b9
```

