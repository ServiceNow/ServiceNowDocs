---
title: GlideCurrencyCode - Scoped, Global
description: The GlideCurrencyCode API provides methods to convert between ISO 4217 alphabetic and numeric codes for a currency.Returns the corresponding alphabetic currency code for a given numeric currency code.Returns the corresponding numeric currency code for a given alphabetic currency code.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencyCode - Scoped, Global

The GlideCurrencyCode API provides methods to convert between ISO 4217 alphabetic and numeric codes for a currency.

Currency code information is also available in the Currency \[fx\_currency\] table, but this API has built-in caching that minimizes the queries issued to fx\_currency.

Use this API to work with third-party APIs that use numeric currency codes, such as credit card network systems.

This API requires the FX Currency \(com.glide.currency2\) plugin, which is available by default. This API is provided within the `sn_currency` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencyCode - getCurrencyCode\(String numberCode\)

Returns the corresponding alphabetic currency code for a given numeric currency code.

|Name|Type|Description|
|----|----|-----------|
|numberCode|String|ISO 4217 numeric currency code.|

|Type|Description|
|----|-----------|
|String|ISO 4217 alphabetic currency code.|

This example returns the alphabetic currency code for the given currency.

```
gs.info(sn_currency.GlideCurrencyCode.getCurrencyCode("840"));
```

Output:

```
USD
```

## GlideCurrencyCode - getNumericCurrencyCode\(String letterCode\)

Returns the corresponding numeric currency code for a given alphabetic currency code.

|Name|Type|Description|
|----|----|-----------|
|letterCode|String|ISO 4217 alphabetic currency code.|

|Type|Description|
|----|-----------|
|String|ISO 4217 numeric currency code.|

This example returns the numeric currency code for United States dollars \(USD\).

```
gs.info(sn_currency.GlideCurrencyCode.getNumericCurrencyCode("USD"));
```

Output:

```
840
```

