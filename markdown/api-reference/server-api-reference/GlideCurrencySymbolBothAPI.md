---
title: GlideCurrencySymbol - Scoped, Global
description: The GlideCurrencySymbol API provides methods to retrieve currency symbols.Returns the corresponding symbol for a given alphabetic currency code.Returns all currency symbols that are currently active on the instance.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencySymbol - Scoped, Global

The GlideCurrencySymbol API provides methods to retrieve currency symbols.

Symbol information is also available in the Currency \[fx\_currency\] table, but this API has built-in caching that minimizes the queries issued to fx\_currency.

This API allows you to work with currency symbols anywhere on the ServiceNow AI Platform, not just in [Currency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/configure-and-use-default-currency-fields.md) and [FX Currency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/currency-administration/fx-currency.md) fields.

This API requires the FX Currency \(com.glide.currency2\) plugin, which is available by default. This API is provided within the `sn_currency` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencySymbol - getCurrencySymbol\(String letterCode\)

Returns the corresponding symbol for a given alphabetic currency code.

|Name|Type|Description|
|----|----|-----------|
|letterCode|String|ISO 4217 alphabetic currency code.|

|Type|Description|
|----|-----------|
|String|Currency symbol for the given code.|

This example returns the currency symbol for United States dollars \(USD\).

```
gs.info(sn_currency.GlideCurrencySymbol.getCurrencySymbol("USD"));
```

Output:

```
$
```

## GlideCurrencySymbol - getSortedActiveCurrencySymbols\(\)

Returns all currency symbols that are currently active on the instance.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_n3t_vp4_nfc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Array of currency symbol objects that are currently active on the instance. Symbols are returned in sorted order by their Unicode code, which is also used when ordering by symbol in the Currency \[fx\_currency\] table.

```
[
  {
    "code": "String",
    "symbol": "String"
  }
]
```

</td></tr><tr><td>

&lt;Array&gt;.code

</td><td>

Currency code.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.symbol

</td><td>

Currency symbol.Data type: String

</td></tr></tbody>
</table>This example lists each currency code and symbol that is currently active on the instance.

```
var symbols = sn_currency.GlideCurrencySymbol.getSortedActiveCurrencySymbols();
for (idx in symbols) {
    gs.info(symbols[idx]["code"] + ": " + symbols[idx]["symbol"]);
};
```

Output:

```
USD: $
CHF: CHF
GBP: £
JPY: ¥
EUR: €
```

