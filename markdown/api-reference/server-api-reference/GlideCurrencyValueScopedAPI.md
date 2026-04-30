---
title: GlideCurrencyValue - Scoped
description: The GlideCurrencyValue API provides methods that return the currency code and original currency from an associated GlideCurrencyParser.parse\(\) call.Returns the currency amount originally passed into the associated GlideCurrencyParser.parse\(\) call.Returns the currency code used to parse the currency in the associated GlideCurrencyParser.parse\(\) call.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencyValue- Scoped

The GlideCurrencyValue API provides methods that return the currency code and original currency from an associated GlideCurrencyParser.parse\(\) call.

This class runs is in the `sn_currency` namespace.

**Note:** There is no constructor for this class.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencyValue - getAmount\(\)

Returns the currency amount originally passed into the associated GlideCurrencyParser.parse\(\) call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Original currency passed into the parse\(\) method.|

This example shows how to call the method.

```
var gp = new sn_currency.GlideCurrencyParser(); 
gp.setLocale("eng", "USA");  
var cv = gp.parse("USD;1234.56"); 
gs.info('Original currency amount: ' + cv.getAmount());

```

Output:

```
Original currency amount: 1234.56
```

## GlideCurrencyValue - getCurrencyCode\(\)

Returns the currency code used to parse the currency in the associated GlideCurrencyParser.parse\(\) call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Three-letter ISO currency code used to parse the currency.|

This example shows how to call the method.

```
var gp = new sn_currency.GlideCurrencyParser(); 
gp.setLocale(eng, USA); 
var cv = gp.parse("USD";"1234.56"); 
gs.info('Parsed currency code: ' + cv.getCurrencyCode());

```

Output:

```
Parsed currency code: USD
```

